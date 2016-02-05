몽고 DB 사용하기
====

사용할 컬렉션의 추가는 `Database/Mongo/Mongo.Collection.cs` 파일을 수정합니다.
```cs
public partial class Mongo
{
   public static IMongoCollection<Model.Player> players { get; private set; }
}
```
이 곳에 `public static`의 컬렉션 프로퍼티 선언을 추가하는 것 만으로도 값이 자동으로 채워집니다.

추가한 프로퍼티는 아래 코드와 같이 접근할 수 있습니다.
```cs
var players = Database.Mongo.Mongo.players;
```

공식 도큐먼트
----
[MongoDB C# Driver Quick Tour](http://mongodb.github.io/mongo-csharp-driver/2.0/getting_started/quick_tour/)
