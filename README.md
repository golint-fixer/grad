# grad

grad provides feature for feed detection from html document.

## Install

```
go get github.com/yukihir0/grad
```

## How to use

```
resp, err := http.Get("...")
if err != nil {
  return
}
defer resp.Body.Close()

feeds := grad.DetectFeed(resp.Body)
for _, feed := range feeds {
  fmt.Println(feed)
}
```

## License

Copyright &copy; 2015 yukihir0
