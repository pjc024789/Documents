����� �߰��ϱ�
====

�޼ҵ带 �����ϴ°����� �ڵ����� ������� �߰��˴ϴ�.<br>

```c#
public class Player {
  public async Task<RespPacket> GetProfile(
    ReqPacket packet, RespPacket) { 
    /* .... */
  }
}
```
�� �޼ҵ�� �ڵ����� /player/getProfile �� ����õ˴ϴ�.

������
----
* Ŭ���� �̸��� ù���ڴ� �ҹ���ȭ �˴ϴ�.
* �޼ҵ� �̸��� ù���ڴ� �ҹ���ȭ �˴ϴ�.
* �ܴ̿� ������� �ʽ��ϴ�.

����
----

ReqestPacket���� Ư���� ���(�α���) ���� �����ϰ�� ��κ��� playerId�� accessToken�� �����ϰ� �ֽ��ϴ�.
�̷��� �����κ��� �ڵ����� ������ ���ɴϴ�.

```c#
public class Player {
  public async Task<RespPacket> SetNickname(
    ReqPacket packet, RespPacket, Model.Session session) { 
    /* .... */
  }
}
```

�� �ڵ忡�� session�� ReqPacket���κ��� �˻��� ���� ��ü�Դϴ�.