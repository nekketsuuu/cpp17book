## emplaceの戻り値

C++17ではシーケンスコンテナーのemplace_front/emplace_back、queueとstackのemplaceが構築した要素へのリファレンスを返すように変更された。

そのため、C++14では以下のように書いていたコードが、

~~~cpp
int main()
{
    std::vector<int> v ;

    v.emplace_back(0) ; // void
    int value = v.back() ;
}
~~~

以下の様に書けるようになった。

~~~cpp
int main()
{
    std::vector<int> v ;

    int value = v.emplace_back(0) ;
}
~~~
