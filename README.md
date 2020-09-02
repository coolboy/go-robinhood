你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
[![GoDoc](https://godoc.org/astuart.co/go-robinhood?status.svg)](https://godoc.org/astuart.co/go-robinhood)

# Robinhood the rich and feeding the poor, now automated

> Even though robinhood makes me poor

## Notice

If you have used this library before, and use credential caching, you will need
to remove any credential cache and rebuild if you experience errors.

## General usage

```go
cli, err := robinhood.Dial(&robinhood.OAuth{
  Username: "andrewstuart",
  Password: "mypasswordissecure",
})

//err

i, err := cli.GetInstrumentForSymbol("SPY")

//err

o, err := cli.Order(i, robinhood.OrderOpts{
  Price: 100.0,
  Side: robinhood.Buy,
  Quantity: 1,
})

//err

time.Sleep(5*time.Second) //Let me think about it some more...

//Ah crap, I need to buy groceries.

err := o.Cancel()

if err != nil {
  //Oh well
}
```
