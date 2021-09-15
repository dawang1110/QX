把下面四个重写和四个定时全加上，获取账号1的阅读body时，记得把其他3个重写给禁止了，弄其他账号时同理。
获取越多body越好，理论上获取500个body能把当天的阅读量完成。
获取完body，去boxjs中把body复制粘贴到备忘录或者其他app里，查找"zqkd_param"并将其全部替换成"p"，再回到boxjs中粘贴。
四个账号全部这样弄一遍。



[rewrite_local]
^https?://(ios\.baertt|kandian\.wkandian)\.com/v5/article/complete\.json url script-request-body https://raw.githubusercontent.com/dawang1110/QX/main/zqgetbody1.js
^https?://(ios\.baertt|kandian\.wkandian)\.com/v5/article/complete\.json url script-request-body https://raw.githubusercontent.com/dawang1110/QX/main/zqgetbody2.js
^https?://(ios\.baertt|kandian\.wkandian)\.com/v5/article/complete\.json url script-request-body https://raw.githubusercontent.com/dawang1110/QX/main/zqgetbody3.js
^https?://(ios\.baertt|kandian\.wkandian)\.com/v5/article/complete\.json url script-request-body https://raw.githubusercontent.com/dawang1110/QX/main/zqgetbody4.js

[task_local]
2 */2 * * * https://raw.githubusercontent.com/dawang1110/QX/main/read1.js , tag=ztxtop中青自动阅读账号1, img-url=https://ghproxy.com/https://raw.githubusercontent.com/erdongchanyo/icon/main/taskicon/Youth.png, enabled=true
2 */2 * * * https://raw.githubusercontent.com/dawang1110/QX/main/read2.js , tag=ztxtop中青自动阅读账号2, img-url=https://ghproxy.com/https://raw.githubusercontent.com/erdongchanyo/icon/main/taskicon/Youth.png, enabled=true
2 */2 * * * https://raw.githubusercontent.com/dawang1110/QX/main/read3.js , tag=ztxtop中青自动阅读账号3, img-url=https://ghproxy.com/https://raw.githubusercontent.com/erdongchanyo/icon/main/taskicon/Youth.png, enabled=true
2 */2 * * * https://raw.githubusercontent.com/dawang1110/QX/main/read4.js , tag=ztxtop中青自动阅读账号4, img-url=https://ghproxy.com/https://raw.githubusercontent.com/erdongchanyo/icon/main/taskicon/Youth.png, enabled=true

[mitm]
kandian.wkandian.com
