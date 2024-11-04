# go_test_project



https://go.dev/doc/install
からGOのパッケージをインストール

環境変数のPATHに
 /usr/local/go
を通す

.bashrc のPATHに追記もしくは作成


$ go mod init example/hello 
go: 新しい go.mod: モジュール example/hello を作成しています
で
go.mod
が作成される

$vi hello.go
でgoファイルを作成する

$ go run .
で実行される

Hello.go などに新しくimport したら

$go mod tidy
で参照ライブラリを自動追加すれば更に実行して結果が得られる

package main
import "fmt"
import "rsc.io/quote"   <—— これなど

func main() {
    fmt.Println(quote.Go())
}

これでもgo.modに追加される
$ go get golang.org/x/example/hello/reverse
