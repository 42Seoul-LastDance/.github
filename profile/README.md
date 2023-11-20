# ft_transcendence

> Real-time Multiplayer Pong Game with Chat, OAuth

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![NestJS](https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white)
![NextJS](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white)
![Unity](https://img.shields.io/badge/unity-%23000000.svg?style=for-the-badge&logo=unity&logoColor=white)
![WebGL](https://img.shields.io/badge/WebGL-990000?logo=webgl&logoColor=white&style=for-the-badge)
![Socket.io](https://img.shields.io/badge/Socket.io-black?style=for-the-badge&logo=socket.io&badgeColor=010101)

<br/><br/>

## Login [OAuth]

- user는 42 intranet의 OAuth 시스템을 이용하여 로그인할 수 있어야 한다.
- user는 website에 표시될 unique한 nickname을 선택할 수 있다.
- user는 프로필 이미지를 업로드할 수 있다. 업로드 하지 않는 경우 디폴트 이미지가 설정되어야한다.
- user는 two-factor authentication을 활성화하고 이용할 수 있다. (Google Authenticator 또는 text message를 보내는 것)
- user는 다른 user를 친구로 추가하고 그들의 현재 상태를 볼 수 있다. (online, offline, in a game, 등등)
- 각 user는 자신만의 Match History를 가지고 있어야 하며 로그인한 사람이라면 누구나 볼 수 있어야 한다. (1대1 게임, ladder 게임 등 유의미한 것들.)

  
<img width="600" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/68d4c1d8-4aec-411c-8f2a-a2bc0aa013c9">

<br/><br/>

## Chatting
- user는 channel(chat rooms)를 만들 수 있어야 한다. 종류는 public, private 혹은 password로 보호되는 방이다.
- user는 다른 user들에게 direct message를 볼 수 있어야 한다.
- user는 다른 user를 차단할 수 있어야 한다. 이러한 방법으로, 차단한 user의 메시지를 볼 수 없어야 한다.
- 새로운 channel을 만든 user는 자동으로 channel owner가 된다.
    - channel owner는 channel에 들어오기 위한 비밀번호를 설정, 변경, 삭제할 수 있다.
    - channel owner는 administrator이기도 하다. 또한 다른 User를 administrator로 설정할 수 있다.
    - channel의 administrator는 다른 user를 kick, ban, mute(제한 시간동안) 할 수 있다. 하지만 channel owner는 불가하다.
- user는 채팅 인터페이스를 통해 다른 user를 Pong Game으로 초대할 수 있어야 한다.
- user는 채팅 인터페이스를 통해 다른 플레이어의 프로필을 볼 수 있어야 한다.


<img width="300" alt="Screen Shot 2023-11-10 at 3 27 14 PM" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/f9ee4a97-b3c3-4315-beba-46c3a0f85b26">

<br/>

<img width="400" alt="Screen Shot 2023-11-10 at 3 27 41 PM" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/34cb4545-83eb-4923-81e3-04007fbd155c">

<img width="400" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/bba3c245-0300-44a8-b81f-1c34d1eb209a">

<br/><br/>

## Game
- matchmaking system이 있어야 한다: user는 다른 user와 자동매치가 되기전까지 queue에 join할 수 있다.
- 게임은 original Pong에 부합해야하며 canvas 게임 혹은 3D로 렌더된 게임이어도 된다.
- 커스터마이징 옵션을 제공해야한다. (power-up, different map). 하지만 user가 항상 골라야 하는 것이 아니라 원하는 feature가 없을 땐 기본 버전을 선택할 수 있어야 한다.


<img width="800" alt="Screen Shot 2023-11-10 at 3 28 54 PM" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/2b9a076c-54e9-48f7-a31a-c478f118a73a">

![ezgif com-video-to-gif (4)](https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/866397c7-7aab-45dd-928b-bccf074a5514)

<br/><br/>

## Friend

<img width="400" alt="Screen Shot 2023-11-10 at 3 26 42 PM" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/6d2dfe38-6efe-49dc-a979-34551f2ce17e">
<img width="400" alt="Screen Shot 2023-11-10 at 3 25 46 PM" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/69365572-5334-4a13-a1b9-241821972ea5">


<br/><br/>

## Profile

<img width="600" alt="Screen Shot 2023-11-10 at 3 32 03 PM" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/f61203c3-2cb8-40c3-b1e4-0f7ea2fe8cf9">

<br/><br/>

## Game Socket Communication

<img width="1444" alt="Screen Shot 2023-11-10 at 4 48 57 PM" src="https://github.com/42Seoul-LastDance/ft_transcendence/assets/87380790/e43fb017-8a8e-4754-98b1-068b6f3f0eac">


## Security Concerns
- 데이터베이스에 저장되는 비밀번호는 hashed 상태로 저장되어야 한다.
- 웹 사이트는 SQL injection으로부터 보호되어야 한다.
- 사용자의 입력이나 form에 대해 server-side 검증을 구현해야 한다.
- (모든 보안 관련한 API key, credential, env 변수들은 .env 파일에 로컬 상태로 보관되어야한다.)
