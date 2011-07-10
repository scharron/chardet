Universal Encoding Detector
===========================

Character encoding auto-detection in Python 2 and 3. As smart as your
browser. Open source.

Getting started
---------------

::

    >>> import urllib
    >>> urlread = lambda url: urllib.urlopen(url).read()


::

    >>> import chardet
    >>> chardet.detect(urlread("http://google.cn/"))
    {'encoding': 'GB2312', 'confidence': 0.99}


::

    >>> chardet.detect(urlread("http://yahoo.co.jp/"))
    {'encoding': 'EUC-JP', 'confidence': 0.99}


::

    >>> chardet.detect(urlread("http://amazon.co.jp/"))
    {'encoding': 'SHIFT_JIS', 'confidence': 1}


::

    >>> chardet.detect(urlread("http://pravda.ru/"))
    {'encoding': 'windows-1251', 'confidence': 0.9355}


::

    >>> chardet.detect(urlread("http://auction.co.kr/"))
    {'encoding': 'EUC-KR', 'confidence': 0.99}


::

    >>> chardet.detect(urlread("http://haaretz.co.il/"))
    {'encoding': 'windows-1255', 'confidence': 0.99}


::

    >>> chardet.detect(urlread("http://www.nectec.or.th/tindex.html"))
    {'encoding': 'TIS-620', 'confidence': 0.7675}


::

    >>> chardet.detect(urlread("http://feedparser.org/docs/"))
    {'encoding': 'utf-8', 'confidence': 0.99}

