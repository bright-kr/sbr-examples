sbr-examples
============

일반적인 브라우저 제어 라이브러리를 사용하여 Bright Data의 [Scraping Browsers](https://brightdata.co.kr/products/scraping-browser) 사용 예제를 제공합니다.

- *-basic: 대상 페이지를 간단히 스クレイピング
- *-captcha: 페이지를 열고 CAPTCHA가 해결될 때까지 대기
- *-advanced: スクレイピング 세션 검사, js 스니펫을 사용한 고급 スクレイピング
- *-proxy-location: スクレイピング 전에 プロキシ 위치 변경
- *-file-download: 브라우저의 다운로드 가져오기

How to run examples
-------------------

control panel에서 Scraping Browsers 자격 증명을 가져와야 합니다.
환경 변수 `AUTH`에 `USER:PASS` 형식으로 전달합니다.

for unix shell:
```bash
export AUTH=brd-customer-hl_01234567-zone-scraping_browser:abcdefghijkl
```

for windows cmd:
```cmd
set AUTH=brd-customer-hl_01234567-zone-scraping_browser:abcdefghijkl
```

for powershell:
```powershell
$Env:AUTH = 'brd-customer-hl_01234567-zone-scraping_browser:abcdefghijkl'
```

기본 대상 웹사이트를 변경하려면 `TARGET_URL` 환경 변수도 전달할 수 있습니다.

nodejs
------

필요한 라이브러리를 설치하려면 npm 패키지 매니저를 사용합니다.

```
$ cd nodejs/puppeteer-basic
.../puppeteer-basic$ npm install
.../puppeteer-basic$ node scrape.js
```

python
------

필요한 라이브러리를 설치하려면 pip 패키지 매니저를 사용합니다.

```
$ cd python/playwright-async-basic
.../playwright-async-basic$ pip3 install -r requirements.txt
.../playwright-async-basic$ python3 scrape.py
```

csharp
------

dotnet 유틸리티를 사용하여 필요한 라이브러리를 설치하고, 빌드 및 실행합니다.

```
$ cd csharp/puppeteer-basic
.../puppeteer-basic$ dotnet run
```

java
----

maven 도구를 사용하여 필요한 라이브러리와 함께 실행 가능한 jar 파일을 패키징합니다.

```
$ cd java/playwright-basic
.../playwright-basic$ mvn package
.../playwright-basic$ java -jar target/sbr-examples-1.0.jar
```

golang
------

go toolchan을 사용하여 필요한 라이브러리를 설치하고, 빌드 및 실행합니다.

```
$ cd golang/playwright-basic
.../golang/playwright-basic$ go get
.../golang/playwright-basic$ go run scrape.go
```