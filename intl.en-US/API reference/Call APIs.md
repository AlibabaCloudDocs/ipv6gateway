# Call APIs

IPv6 Gateway and VPC use the same service address \(endpoint\). When you call an IPv6 Gateway API, an HTTP GET request is sent to the API service address of IPv6 Gateway and the system responds according to the parameters set in the request. Both the request and the response are UTF-8-encoded.

## Request syntax

IPv6 Gateway APIs are of the RPC type. You can call IPv6 Gateway APIs by sending HTTP GET requests.

The request syntax is as follows:

```
http://Endpoint/?Action=xx&Parameters 
```

where:

-   Endpoint: The endpoint of IPv6 Gateway APIs is `vpc.aliyuncs.com`.
-   Action: the name of this action. For example, if you need to create an IPv6 Gateway, the action is CreateIpv6Gateway.
-   Version: the version of the API to use. The current IPv6 Gateway API version is 2016-04-28.
-   Parameters: the request parameters. Separate multiple parameters by using ampersands \(&\).

    Request parameters include common parameters and API-specific parameters. Common parameters include API version and identity authentication information among other parameters. For more information, see [Common parameters](/intl.en-US/API reference/HTTP Requests/Common parameters.md).


The following is an example of calling CreateIpv6Gateway to create an IPv6 Gateway:

**Note:** The following code has been edited to improve readability.

```
https://vpc.aliyuncs.com/?Action=CreateIpv6Gateway
&Format=xml
&Version=2016-04-28 
&Signature=xxxx%xxxx%3D 
&SignatureMethod=HMAC-SHA1
&SignatureNonce=15215528852396 
&SignatureVersion=1.0
&AccessKeyId=key-test
&Timestamp=2012-06-01T12:00:00Z
…
```

## API authorization

To maintain account security, we recommend that you use the Access Keys \(AKs\) of RAM users to call APIs. Before a RAM user can start to call APIs, you must grant the RAM user permission by creating an authorization policy and attaching the policy to the RAM user.

For a list of IPv6 Gateway resources and APIs that can be authorized, see [RAM user authorization](/intl.en-US/API reference/RAM user authorization.md).

## API signature

To ensure the security of your API, you must sign the API request. Alibaba Cloud then uses the signature in the request to verify the identity of the user who calls the API.

Smart Access Gateway uses AccessKeyId and AccessKeySecret for symmetric encryption to verify the identity of the caller. AKs are certificates that Alibaba Cloud issues to Alibaba Cloud accounts and RAM users for authentication. It is similar to a logon password. The AccessKeyID is used to identify the visitor's identity. The AccessKeySecret is the key used to encrypt the signature string. The server uses the AccessKeySecret to decrypt the signature string. The AccessKeySecret must be kept confidential.

For an RPC API, you must add the signature to the API request in the following format:

`https://endpoint/?SignatureVersion=*1.0*&SignatureMethod=*HMAC-SHA1*&Signature=*XXXX%3D&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx*`

Take the API call of CreateIpv6Gateway as an example. If your AccessKeyID is `testid`, and your AccessKeySecret is `testsecret`, then, the URL in the signature is as follows:

```
http://vpc.aliyuncs.com/?Action=CreateIpv6Gateway
&Timestamp=2016-05-23T12:46:24Z 
&Format=XML
&AccessKeyId=testid 
&SignatureMethod=HMAC-SHA1
&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx 
&Version=2014-05-26
&SignatureVersion=1.0
```

To generate the signature, follow these steps:

1.  Create the string to be signed by using the request parameter.

    ```
    GET&%2F&AccessKeyId%3Dtestid&Action%3DCreateIpv6Gateway&Format%3DXML&SignatureMethod%3DHMAC-SHA1&SignatureNonce%3D3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx&SignatureVersion%3D1.0&TimeStamp%3D2016-02-23T12%253A46%253A24Z&Version%3D2014-05-15
    ```

    .

2.  Calculate the HMAC value of the string.

    Add an ampersand \(&\) after the AccessKeySecret to add the key of the HMAC value. In this example, the key is `testsecret&`.

    ```
    CT9X0VtwR86fNWS********juE=
    ```

3.  Add the signature to the request parameter.

    ```
    http://vpc.aliyuncs.com/?Action=CreateIpv6Gateway
    &Timestamp=2016-05-23T12:46:24Z 
    &Format=XML 
    &AccessKeyId=testid 
    &SignatureMethod=HMAC-SHA1 
    &SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0axxxxxxxx 
    &Version=2014-05-26
    &SignatureVersion=1.0
    &Signature=XXXX%3D
    ```


