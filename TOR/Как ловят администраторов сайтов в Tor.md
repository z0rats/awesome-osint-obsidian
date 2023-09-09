[[TOR]]

28.07.2023

Вот нес­коль­ко инс­тру­мен­тов, которые помога­ют иссле­довать ноды Tor:

- [TOR Node List](https://www.dan.me.uk/tornodes) — спи­сок нод;
- [ExoneraTor](https://metrics.torproject.org/exonerator.html) — про­вер­ка IP на исполь­зование в качес­тве нод Tor;
- [Onionite](https://github.com/lukechilds/onionite) — информа­ция о нодах;
- [Tor Metrics](https://metrics.torproject.org/) — информа­ция о нодах;
- [Collector Tor](https://collector.torproject.org/archive/relay-descriptors/microdescs/) — архив IP и пор­тов узлов.

[TorWhois](https://torwhois.com/) — неч­то вро­де сер­виса Whois для Tor. Поз­воля­ет получить информа­цию об откры­тых пор­тах, сер­тифика­тах, клю­чах и информа­цию о robots.txt.

### Структура сайтов

Сай­ты в Tor исполь­зуют обык­новен­ные CMS, как и сай­ты в «клир­нете». Конеч­но, внут­ри всё те же HTML, CSS и дру­гие при­выч­ные тех­нологии. То есть тут нет ничего уди­витель­ного и нового. А исполь­зование популяр­ных тех­нологий, конеч­но, откры­вает воз­можность для авто­мати­зации ауди­та в целях раз­ведки. Для это­го есть:

- Onionscan (аудит onion-сай­та);
- Onion Nmap (Nmap для onion-сай­та);
- OWASP ZAP (ска­нер);
- Nikto (ска­нер);
- WPScan (ска­нер);
- Burp Suite (ска­нер);
- Wapiti (ска­нер);
- [спи­сок уяз­вимос­тей на Mitre.org](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=tor).

### Теневая экономика

По­луча­ется, что мож­но уста­новить, каким обменни­ком поль­зует­ся про­давец, если знать адрес его крип­товалют­ного кошель­ка. Для это­го дос­таточ­но визу­али­зиро­вать его активность с помощью спе­циаль­ной прог­раммы. На кошель­ке обменни­ка, конеч­но же, будет огромное чис­ло тран­закций и немалая сум­ма денег.

Ви­зуали­зато­ры зачас­тую плат­ные, но есть и нес­коль­ко бес­плат­ных:

- [Breadcrumbs](https://www.breadcrumbs.app/);
- [OXT.ME](https://oxt.me/);
- [Blockpath](https://blockpath.com/).

### Поисковики

По­иско­вики и дор­ки (рецеп­ты зап­росов) всег­да были глав­ным ору­жием сов­ремен­ного OSINT-спе­циалис­та, и в сети Tor всё точ­но так же. Давай пос­мотрим, какие поис­ковики ищут по дар­кве­бу.

Вот поис­ковые сис­темы, дос­тупные в кли­рене­те, и индекси­рующие onion-сай­ты:

- [Onion Search Engine](https://onionengine.com/);
- [Torry](https://www.torry.io/);
- [OnionLand Search](https://onionlandsearchengine.net/);
- [Tor Search](https://torsearch.com/);
- [OnionSeach](https://github.com/megadose/OnionSearch);
- [DuckDuckGo](https://duckduckgo.com/).

Спи­сок поис­ковых сис­тем, у которых есть сай­ты в сети Tor (ссыл­ки при­веде­ны на onion-адре­са):

- [DuckDuckGo](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/);
- [Not Evil](http://notevilmtxf25uw7tskqxj6njlpebyrmlrerfv5hc4tuq7c7hilbyiqd.onion/);
- [Ahmia](http://juhanurmihxlp77nkq76byazcldy2hlmovfu2epvl5ankdibsot4csyd.onion/);
- [Haystak](http://haystak5njsmn2hqkewecpaxetahtwhsbsa64jom2k22z5afxhnpxfid.onion/);
- [Torch](http://torchdeedp3i2jigzjdmfpn5ttjhthh5wbmda2rr3jvqjg5p77c54dqd.onion/);
- [Demon](http://srcdemonm74icqjvejew6fprssuolyoc2usjdwflevbdpqoetw4x3ead.onion/).

Кста­ти, о темати­чес­ких форумах. Есть вики, которые кол­лекци­они­руют ссыл­ки на сай­ты в дар­кве­бе, и отту­да лег­ко почер­пнуть под­борку адре­сов кри­миналь­ных форумов. Вот некото­рые из них:

- [The Hidden Wiki](https://thehiddenwiki.org/);
- [IACA DarkWeb](https://iaca-darkweb-tools.com/);
- [DarkWeb Links](https://darkweb-links.co/dark-web-links/);
- [The DarkWeb Links](https://www.thedarkweblinks.com/).

### Краулеры, спайдеры, скреперы

Эти инс­тру­мен­ты полез­ны при ана­лизе сай­тов в сети Tor. Они помога­ют соб­рать информа­цию о фотог­рафи­ях, дирек­тори­ях и самую раз­ную информа­цию о струк­туре сай­тов. Инте­рес­ны они тем, что дают мак­симум све­дений о том, что про­исхо­дит на сай­те, без посеще­ния самого сай­та.

Нач­нем с кра­уле­ров, их мож­но исполь­зовать для сбо­ра опре­делен­ного типа дан­ных на сай­те, к при­меру фото, видео, тек­ста и так далее. Нап­ример, ты хочешь переб­рать все фото на сай­те и най­ти те, которые содер­жат метадан­ные.

Вот нес­коль­ко кра­уле­ров для Onion:

- [TorBot](https://github.com/DedSecInside/TorBot);
- [OnionBot](https://github.com/Flobin/OnionBot);
- [OnionScan](https://onionscan.org/);
- [VigilantOnion](https://github.com/andreyglauzer/VigilantOnion);
- [OnionIngestor](https://github.com/danieleperera/OnionIngestor).

Скре­перы работа­ют по задан­ному алго­рит­му, который опре­деля­ет, какие дан­ные нуж­но собирать и как их извле­кать. Обыч­но они дела­ют зап­росы к сер­веру, а затем ана­лизи­руют получен­ный HTML, что­бы извлечь нуж­ную информа­цию. В ход идут раз­ные методы раз­бора стра­ниц — пар­синг HTML, поиск по тегам и клас­сам CSS, регуляр­ные выраже­ния и так далее. Час­то сай­ты выг­ружа­ются целиком для даль­нейше­го ана­лиза.

Вот некото­рые прог­раммы и биб­лиоте­ки для скре­пин­га:

- [Scrapy](https://scrapy.org/);
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/);
- [Selenium](https://www.selenium.dev/);
- [Puppeteer](https://github.com/puppeteer/puppeteer);
- [Frontera](https://github.com/scrapinghub/frontera).

Па­уки же пред­назна­чены для индекса­ции сотен и тысяч ссы­лок. Для Tor сущес­тву­ют [Onioff](https://github.com/k4m4/onioff) и [Onion Spider](https://github.com/ne-bknn/onion_spider).