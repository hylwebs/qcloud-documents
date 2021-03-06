## 1. API Description
 API ModifyForwardLBSeventhListener is used to modify the attributes of forwarding cloud load balancer layer-7 listener.
 
Domain for API access: lb.api.qcloud.com


## 2. Request Parameters

   The following request parameter list only provides API request parameters. Common request parameters need to be added when the API is called. For more information, refer to [Common Request Parameters](/doc/api/244/4183). The Action field for this API is ModifyForwardLBSeventhListener.
 
| Parameter Name | Required | Type | Description |
|-----|------|--------|-----------|
| loadBalancerId | Yes | String | Uniform ID of cloud load balancer instance, i.e. unLoadBalancerId. It can be queried by entering 1 or -1 in input parameter "forward" field of API <a href="https://www.qcloud.com/doc/api/244/%E6%9F%A5%E8%AF%A2%E8%B4%9F%E8%BD%BD%E5%9D%87%E8%A1%A1%E5%AE%9E%E4%BE%8B%E5%88%97%E8%A1%A8" title="DescribeLoadBalancers">DescribeLoadBalancers</a>. |
| listenerId | Yes | String | ID of application-based cloud load balancer listener. It can be queried through API DescribeForwardLBListeners. |
| listenerName | No | String | Name of application-based cloud load balancer listener. |
| SSLMode | No | String | Authentication mode of HTTPS listener. unidirectional: unidirectional authentication; mutual: mutual authentication. |
| certId | No | String | New server certificate ID of HTTPS listener. |
| certCaId | No | String | New client certificate ID of HTTPS listener. |
| certCaContent | No | String | New client certificate content of HTTPS listener. |
| certCaName | No | String | New client certificate name of HTTPS listener. |
| certContent | No | String | New server certificate content of HTTPS listener. |
| certKey | No | String | New server certificate key of HTTPS listener. |
| certName | No | String | New server certificate name of HTTPS listener. |

## 3. Response Parameters
 
 
| Parameter Name | Type | Description |
|-------|---|---------------|
| code | Int | Common error code; 0: Succeeded; other values: Failed. For more information, please refer to [Common Error Code](/doc/api/244/1530) in the Error Code page. |
| message | String | Module error message description depending on API. |
| codeDesc | String | Error code. For a successful operation, "Success" will be returned. For a failed operation, a message describing the failure will be returned. |
| requestId | Int | Request task ID. The operation status can be queried through API [DescribeLoadBalancersTaskResult](/doc/api/244/4007). |

## 4. Example
 
Input
```
https://lb.api.qcloud.com/v2/index.php?Action=ModifyForwardLBSeventhListener
&<Common request parameters>
&loadBalancerId=lb-ltkip4do
&listenerId=lbl-6hkiqc6c
&SSLMode=unidirectional
```
Output
```
{
    "code": 0,
    "message": "",
    "codeDesc": "Success",
    "requestId": 18642
}

```



