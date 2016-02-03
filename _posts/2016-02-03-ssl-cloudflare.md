---
layout: post
title: Cloudflare를 이용해서 Github Pages 블로그에 SSL을 적용했다
excerpt: Cloudflare에서 간단한 설정을 하는 것만으로 Github Pages에 만든 내 블로그에 SSL을 적용할 수 있었다.
---

이후에 나올 크롬에서는 SSL을 적용하지 않은 사이트를 안전하지 않은 사이트로 표기한다고 한다.[^1] 이미 전부터 구글은 SSL을 적용한 사이트의 구글 검색 랭킹을 상향하는 작업을 하고 있었다.[^2] 그래서 시험삼아 이 블로그에도 SSL을 적용해봤다. 

Cloudflare를 쓰고 있다면 아주 간단한 일이다. Page rule에서 모두 https로 리다이렉트 되도록 설정해주고, HSTS 설정만 해주면 끝이다. 그러면 이제 블로그로 접속하는 모든 커넥션은 SSL이 적용된다.

사실 이 블로그는 Jekyll로 운영되는데다가, 폼도 쓰지 않기 때문에 웹브라우저를 통해서 개인적인 정보가 전송될 일이 없다. 그래서 SSL이 특별히 필요하지는 않다. 하지만 구글의 정책에 따라 한 번 재미삼아 해볼만한 일이다. 단, SSL을 적용하면 로딩 속도가 조금 느려진다. 그걸 감안하고 적용하는 것이 좋을 것이다.










[^1]: [Google Will Soon Shame All Websites That Are Unencrypted @Motherboard](http://motherboard.vice.com/read/google-will-soon-shame-all-websites-that-are-unencrypted-chrome-https)
[^2]: [Google Starts Giving A Ranking Boost To Secure HTTPS/SSL Sites @Search Engine Land](http://searchengineland.com/google-starts-giving-ranking-boost-secure-httpsssl-sites-199446)