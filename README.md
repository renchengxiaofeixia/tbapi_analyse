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

### 千牛MTOP接口
```js
// 好友列表
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.taobao.wireless.amp2.im.relation.rebase',
      param:{
	"accessKey": "qianniu-pc",
	"accessSecret": "qianniu-pc-secret","accountType": "3",
	"bottomOffset": 100,
	"topOffset": 100
},
      httpMethod: 'post',
      version: '1.0',
    },
  }); 

//千牛店铺子账号在线状态
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.taobao.qianniu.cloudkefu.accountstatus.getbyid',
      param: {pageSize: 100},
      httpMethod: 'post',
      version: '1.0',
    },
  }); 

//专属客服卡片
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.taobao.qianniu.bcpush.send.subscribecard',
      param: {"subscriberNick":"淘宝昵称"},
      httpMethod: 'post',
      version: '1.0',
    },
  }); 

//添加好友
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.taobao.wireless.amp2.im.relation.addcontact',
      param:{
	"accessKey": "qianniu-pc",
	"accessSecret": "qianniu-pc-secret",
	"accountType": "3",
	"contactReq": "{\"targetAccountId\":\"淘宝UserId\",\"targetAccountType\":\"3\",\"targetNickName\":\"\",\"targetRemarkName\":\"\",\"groupId\":0,\"bizType\":\"-1\",\"relationType\":0,\"ext\":{\"msg\":\"验证信息\"}}"
},
      httpMethod: 'post',
      version: '1.0',
    },
  }); 


//删除好友
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.taobao.wireless.amp2.im.relation.deletecontact',
      param: {"accessKey":"qianniu-pc","contactlist":"[{\"targetAccountId\":\"淘宝UserId\",\"targetAccountType\":3,\"bizType\":\"-1\",\"relationType\":0}]","accessSecret":"qianniu-pc-secret","accountType":"3"},
      httpMethod: 'post',
      version: '1.0',
    },
  }); 
  
 //标星 
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.taobao.qianniu.airisland.tag.batch.update',
      param:{"context":"{\"bizDomain\":\"taobao\"}","tagUpdateParams":"[{\"tagCode\":\"TOP_TYPE_RED\",\"targetId\":\"1597305140\",\"bizExt\":\"{}\",\"entityType\":0,\"bizDomain\":\"taobao\",\"groupCode\":\"QIANNIU_STAR\",\"updateType\":0}]","tenantId":"QIANNIU_RECEPTION"},

      httpMethod: 'post',
      version: '2.0',
    },
  }); 

//订单物流信息
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.cainiao.cilogistics.smart.customer.logistics.detail',
      param:{"tradeId":"订单号","sellerId":"0"},

      httpMethod: 'post',
      version: '1.0',
    },
  }); 

//快捷短语
await QN.app.invoke({
    api: 'invokeMTopChannelService',
    query: {
      method: 'mtop.taobao.qianniu.quickphrase.get',
      param: {from:'',version:1.0},
      httpMethod: 'post',
      version: '1.0',
    },
  }); 
// 核对订单卡片
imsdk.invoke('application.invokeMTopChannelService', {
            method: 'mtop.taobao.bcpush.order.check.card.send',
            param:{bizOrderId:'订单号',buyerNick:'淘宝昵称'},
            httpMethod: 'post',
            version: '1.0'
        });
//邀请下单
await imsdk.invoke('application.invokeMTopChannelService', {
    method: 'mtop.taobao.qianniu.airisland.invite.order.send',
    param: {
        buyerNick: '淘宝昵称',
        itemProps: JSON.stringify([{
            itemId: 商品id,
            skuId: 'skuid',
            quantity: 数量,
            context: {}
        }])
    },
    httpMethod: 'post',
    version: '1.0'
});
//转接
imsdk.invoke('application.invokeMTopChannelService', {
            method: 'mtop.taobao.qianniu.cloudkefu.forward',
            param:{"buyerId":buyerid,"toId":toid,"reason":"","options":"{\"appCid\":\"ccode\",\"buyerDomain\":\"cntaobao\",\"loginDomain\":\"cntaobao\"}"},
            httpMethod: 'post',
            version: '3.0'
        });
```
