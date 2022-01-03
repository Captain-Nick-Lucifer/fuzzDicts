# fuzzDicts
Web Pentesting Fuzz dictionary, one is enough.

## log

Update from time to time. It is recommended to git pull and update synchronously before use.


  **Sharing dictionary is recommended to submit directly to PR**

20210608:

* Added a [Remote Code Execution (Unix and Windows)](https://ansar0047.medium.com/remote-code-execution-unix-and-windows-4ed3367158b3) under the dictionary of rcePayloads.

20201202:

* A variant of the admin directory given by the master [Se7en](https://github.com/r00tSe7en) has been updated under the directory dictionary.

20200510:

* A new pinyin of the Baijia surname top3000 is added under the user name dictionary, after removing the duplicate 188 entries, Attack!!!.


20200420:

* Incorporate a pr submitted by [lanyi1998](https://github.com/lanyi1998), test the commonly used mobile phone number top300+, put it in the user name dictionary, you can try it during bottleneck testing; add a copy provided by the team’s Child master A weak password dictionary for a certain group.

20200410:

* Added the file list in the /etc/ directory of centOS and AIX hosts, and put them in the ssrfDict directory. In actual combat, the difference between aix and other systems is quite big, so you can figure it out by yourself.

20200406:

* Incorporate a pr submitted by [lewiswu1209](https://github.com/lewiswu1209) with password top19576.


20200221:

* Update the webshell password dictionary enhanced by the master [makoto56](https://github.com/makoto56). During the resignation study, there will not be too many web test tasks before graduation (and I don’t want to continue playing web anymore), The update frequency of the dictionary will be reduced a lot. If you have a small partner who wants to maintain it together, you can contact me.

20200211:

* Added a new lot dictionary, the data comes from the weak passwords of 50w Internet lot devices sent by others in the tg group, extracted by the master [sunu11](https://github.com/sunu11), and on this basis domestic data has been added . When I encountered an unknown device, I was shocked, and I used the dictionary to get twice the result with half the effort.

20200115:

* The xss dictionary adds 210 official burp payloads and put them in the [burpXssPayload.txt](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/easyXssPayload/burpXssPayload.txt) file in the easyXssPayload directory.

* The user name dictionary adds the ids of the 2018-2020 youth security circles, the data source [Security-Data-Analysis-and-Visualization](https://github.com/404notf0und/Security-Data-Analysis-and- Visualization), separated the three fields of id, blog domain name, and github ID. Put it in [sec_ID.txt](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/userNameDict/sec_id.txt) in the userNameDict directory. When encountering a shell, go and hit it first. Self-built waf and these ids are marked as The blacklist keyword is right.

* Other optimizations and updates.


20200106:

* 100+ new payloads have been added to the xss dictionary and merged into this project.

20200104:

* Optimize the parameter dictionary again, thanks to [key师傅](https://github.com/gh0stkey) for the correction.

20191219:

* Use the regular `(\W)` to filter many invalid parameters, such as spaces (){}, etc., and allow the existence of -, re-merge the parameter dictionary to remove the duplicates, and put them in AllParam.txt, thank you milk right Master’s feedback.

20191214:

* Recently, I have sorted out the vulnerabilities of each CMS. I downloaded more than 50 CMS before and after. By the way, I collected some parameters again, and the volume of parameter.txt increased to 5859. (Formerly 2800+)

20191106:

* A quick reference table for the default user name and password of Huawei security products has been newly added under the password dictionary.

20191026:

* The parameter dictionary was found to be cumbersome during use, so the recently collected dictionaries and the dictionaries in some excellent tools were merged and repeatedly put into AllParam.txt, a total of 51219 entries are recommended.

20191022:

* A new tool named [Arjun](https://github.com/s0md3v/Arjun) has been added under the parameter dictionary, which is much more powerful than the original script. The dictionary is in the db directory.

20190928:

* Added the wifi password top2000 dictionary copied from [Pig Pig Man Github](https://github.com/ring04h) under passwordDict.

20190819:

* Added a new common vulnerability directory under directoryDicts, it is recommended to use all.txt directly

* Added a list of weak passwords for common security devices/routers/middleware/services under passwodDict. However, it is recommended to use the strong and weak password dictionary RW_Password, because many units have to set the passwords complicatedly under the pressure of the security. In order to facilitate the memorization of these passwords, these passwords are basically regular, and thus the strong and weak passwords are born. It's easy to use.
* For other updates, some dictionaries in this update were collected from [SaiDict](https://github.com/Stardustsky/SaiDict), and they were carefully removed when merging.

20190811:

* I uploaded the dictionary I usually use for blasting subdomains (extracted from tools such as subDomainsBrute, layer, and merged to remove duplicates, and then merged with some of the dictionaries I generated). It is recommended to use main.txt, the other is the younger brother.

20190801:

* Incorporated a [r35tart](https://github.com/r35tart/RW_Password) a very good dictionary of "strong and weak passwords" compiled by the master (that is, it looks complicated, but it is a password that many people actually use)

20190615:

* Incorporated a [foreign dictionaries](https://github.com/emadshanab/WordLists-20111129) I feel that the classification is a bit messy. After the exam, I will reorganize it.

## content

* [Parameter fuzz dictionary](#parameter fuzz dictionary)
* [Xss Fuzz dictionary](#xss-fuzz dictionary)
* [Username dictionary](#Username dictionary)
* [Password dictionary](#Password dictionary)
* [Catalog Dictionary](#Catalog Dictionary)
* [sql-fuzz dictionary](#sql-fuzz dictionary)
* [ssrf-fuzz dictionary](#ssrf-fuzz dictionary)
* [XXE dictionary](#XXE dictionary)
* [ctf dictionary](#ctf dictionary)
* [Api dictionary](#Api dictionary)
* [Router background dictionary](# Router background dictionary)
* [File suffix Fuzz](#File suffix Fuzz)
* [js file dictionary](#jsfile dictionary)
* [SubdomainDictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/subdomainDicts)



Recommended tools: [burpsuite](https://portswigger.net/burp/),[sqlmap](https://github.com/sqlmapproject/sqlmap),[xssfork](https://github.com/bsmali4/ xssfork),[Wfuzz](https://github.com/xmendez/wfuzz/),[webdirscan](https://github.com/TuuuNya/webdirscan)

If you have any good dictionaries or suggestions, please submit an issue to me.


## [Parameter Fuzz Dictionary](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/paramDict)

```
https://github.com/TheKingOfDuck/fuzzDicts/blob/master/paramDict/parameter.txt
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/parameter.jpg)



Collected from common PHP frameworks/CMS such as `ThinkPHP`, `yii2`, `phphub`, `Zblog`, `DiscuzX`, `WordPress`, etc.

Tips: For example, http://127.0.0.1/1.php, which is regarded as a suspicious file, and fuzz param select GET, POST AND (POST JSON) AND (GET Route) AND cookie param


## [Xss Fuzz Dictionary](https://github.com/TheKingOfDuck/easyXssPayload/blob/master/easyXssPayload.txt)

```
https://github.com/TheKingOfDuck/easyXssPayload/blob/master/easyXssPayload.txt
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/xss.jpg)

Collected from `github`.

## [User Name Dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/userNameDict)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/userNameDict
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/username.jpg)


## [Password Dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/passwordDict)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/passwordDict
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/password.jpg)

## [Directory Dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/directoryDicts)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/directoryDicts
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/directory.jpg)


## [SQL Fuzz Dictionary](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/sqlDict/sql.txt)

```
https://github.com/TheKingOfDuck/fuzzDicts/blob/master/sqlDict/sql.txt
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/sql.jpg)


## [ssrf fuzz dictionary](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/ssrfDicts)

```
https://github.com/TheKingOfDuck/fuzzDicts/blob/master/ssrfDicts
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/ssrf.jpg)

Provided by [\xeb\xfe](https://github.com/doge-dog) master.

## [XXE dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/XXEDicts)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/XXEDicts
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/xxe.jpg)

Collected from Baidu.

## [ctf dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/ctfDict)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/ctfDict
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/ctfDict/ctf-wscan/1.gif)

Collected from [kingkaki](https://github.com/kingkaki/ctf-wscan), the compressed package downloaded directly by Baidu during the original collection, I did not see the github link, so I did not mark the source, sorry

## [Api dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/apiDict)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/apiDict/api.txt
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/api.jpg)

The code collected by Zhong Kui is written very cxk my real brother. . .

## [Router background dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/routerDicts)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/routerDicts/pass.txt
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/router.jpg)

## [File suffix Fuzz](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/uploadFileExtDicts)

```
https://github.com/TheKingOfDuck/fuzzDicts/tree/master/uploadFileExtDicts
```

![CoolCat](https://github.com/TheKingOfDuck/fuzzDicts/blob/master/images/fileExt.png)

Collected from https://github.com/c0ny1/upload-fuzz-dic-builder


## [js file dictionary](https://github.com/TheKingOfDuck/fuzzDicts/tree/master/js)

Collected from: https://github.com/7dog7/bottleneckOsmosis
