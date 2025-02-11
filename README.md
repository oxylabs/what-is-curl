# What is cURL and What Does It Mean

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

[<img src="https://img.shields.io/static/v1?label=&message=curl&color=brightgreen" />](https://github.com/topics/curl)

- [Sending requests](#sending-requests)
- [Following redirects](#following-redirects)
- [Connecting through a proxy](#connecting-through-a-proxy)

cURL (client URL) is an open-source command line tool, and a cross-platform library (`libcurl`) used to transfer data between servers, distributed to nearly all new operating systems. cURL programming is used almost everywhere where sending or receiving data through internet protocols is required.

This article gives you an overview of cURL.

For a detailed explanation, see our [blog post](https://oxylabs.io/blog/what-is-curl). 

## Sending requests

To use curl, write curl followed by the URL. This sends a GET request.

```shell
curl https://httbin.org/get 
```

 To send a POST request to a URL, the `-d` (or `–data`) flag is used:

```shell
curl -d "name=something&value=somethingelse" https://jsonplaceholder.typicode.com/posts/
```

Sending such a request should return:

```json
{
  "name": "something",
  "value": "somethingelse",
  "id": 101
}
```

We can also send POST requests in JSON form by adding the header `Content-Type: application/json`:

```shell
curl -H "Content-Type: application/json" --data "{\"data\":\"some data\"}"  https://jsonplaceholder.typicode.com/posts/
```

## Following redirects

Add `-L` to follow redirects:

```shell
curl -L https://google.com
```

## Connecting through a proxy

cURL can be used to connect to any destination through a proxy:

```shell
curl --proxy proxyaddress:port https://jsonplaceholder.typicode.com/
```

Credential details can be sent through the `-U` flag.

```shell
curl --proxy proxy:port -U “username:password” https://jsonplaceholder.typicode.com/
```

Some websites will require authentication by themselves before they accept any connection request. A similar flag `-u` is used for server authentication: 

```shell
curl -u username:password https://jsonplaceholder.typicode.com/
```



If you wish to learn more about cURL, see our [blog post](https://oxylabs.io/blog/what-is-curl).


