라우터 추가하기
====

메소드를 정의하는것으로 자동으로 라우팅이 추가됩니다.<br>

```c#
public class Player {
  public async Task<RespPacket> GetProfile(
    ReqPacket _in, RespPacket _out) { 
    /* .... */
  }
}
```
위 메소드는 자동으로 /player/getProfile 에 라우팅됩니다.

컨벤션
----
* 클래스 이름의 첫글자는 소문자화 됩니다.
* 메소드 이름의 첫글자는 소문자화 됩니다.
* 이외는 변경되지 않습니다.

세션
----

ReqestPacket에는 특수한 경우(로그인) 등을 제외하고는 대부분이 playerId와 accessToken을 포함하고 있습니다.
이러한 정보로부터 자동으로 세션을 얻어옵니다.

```c#
public class Player {
  public async Task<RespPacket> SetNickname(
    ReqPacket _in, RespPacket _out, Model.Session session) { 
    /* .... */
  }
}
```

위 코드에서 session은 ReqPacket으로부터 검색된 세션 객체입니다. 이 세션은 처리마다 자동 저장됩니다.