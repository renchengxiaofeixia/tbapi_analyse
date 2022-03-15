### 非常规参数取值记录

淘宝直通车API：https://subway.simba.taobao.com/

| 参数      | 取值                                                       |
| --------- | ---------------------------------------------------------- |
| sessionId | localStorage.getItem('sid')                                |
| token     | https://subway.simba.taobao.com/bpenv/getLoginUserInfo.htm |

淘宝引力魔方API：https://tuijian.taobao.com/

| 参数         | 取值                                                         |
| ------------ | ------------------------------------------------------------ |
| csrfID       | https://tuijian.taobao.com/api2/member/getInfo.json          |
| dynamicToken | https://g.alicdn.com/mm/display/20220311.140658.727/display/services/jsvm.js |



```js
module.exports = function(n, t, r) {
            n = n || "",
            t = t || 2;
            var e, o, s, u, i, jsvmportal_0_1 = function() {
                var inout = arguments, retval;
                return jsvm_this_run(function() {
                    return eval(arguments[0])
                }, 0),
                retval
            };
            return jsvm_this_run(function() {
                return eval(arguments[0])
            }, 1),
            "" + e(u) + e(i)
}
// dynamicToken 计算方法 
// seedToken,pin,csrfID 都来源于这个接口 https://tuijian.taobao.com/api2/member/getInfo.json
var dynamicToken = jsvmfuc(seedToken, pin, timeStamp)

```
