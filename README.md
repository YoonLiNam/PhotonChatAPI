# PhotonChatAPI
Provides a guide for easy use of ‘ PhotonChatAPI ’.


PhotonChat_Demo DownLoad : [DownLoad](https://drive.google.com/file/d/0BzGm_WSvgeywanFTaU01cWJwU0k/view?usp=sharing)



Photon Chat 기본적인 기능은 이렇게 됩니다.


## PhotonChat 서버와 연결합니다.
<pre><code>
chatClient.Connect(appid, 버전(채팅하는사람들 모두 동일해야함),접속한 유저정보를 photon에 저장)
</code></pre>
## 채팅 채널에 접속합니다.
<pre><code>
chatClient.Subscribe(접속하고자 하는 채널 리스트, 접속하자마자 이전 대화목록 얼마나 받을 것인가)
</code></pre>
## 일반 채팅을 보냅니다.
<pre><code>
chatClient.PublishMessage(채널 이름, 메시지)
</code></pre>
## 비밀 채널에 채팅을 보냅니다.
<pre><code>
chatClient.SendPrivateMessage(메시지 받을 유저,메시지)
</code></pre>

## 각 채널에 날라온 메시지들을 받습니다.
<pre><code>
// OnGetMessages(채널이름, 보낸사람, 메시지)
OnGetMessages(string channelName, string[] senders, object[] messages)
</code></pre>
## 비밀 채널로 본인에게 온 메시지를 받습니다.
<pre><code>
// OnPrivateMessage(보낸사람, 메시지, 비밀채널이름);
OnPrivateMessage(string sender, object message, string channelName)
</code></pre>
