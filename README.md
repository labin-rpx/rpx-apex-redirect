# rpx-apex-redirect

`rpx.co.kr` (www 없는 주소)로 들어온 사람을 `https://www.rpx.co.kr` 로 넘기는 한 장짜리 페이지입니다.

- 왜 따로 있나: 홈페이지는 Cloudflare Pages 에 있는데, 네임서버를 옮기지 않으면 Cloudflare 는 www 없는 주소를 직접 못 받습니다.
  호스팅케이알의 포워딩은 DNS 기록(메일 등)이 있으면 켤 수 없습니다. 그래서 고정 IP 를 주는 GitHub Pages 로 넘기기만 합니다.
- DNS: 호스팅케이알에 `@` A 기록 4개(185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153).
- `404.html` 은 `index.html` 과 같은 내용입니다(어떤 경로로 와도 같은 경로의 www 주소로 넘김).
- 홈페이지 본체: `C:\Users\labin\rpx-home` (저장소 labin-rpx/rpx-home).

나중에 네임서버를 Cloudflare 로 옮기면 이 저장소와 A 기록 4개는 지워도 됩니다.
