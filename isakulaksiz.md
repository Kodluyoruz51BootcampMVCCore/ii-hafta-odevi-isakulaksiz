# REST vs SOAP

| REST  | SOAP |
| ------------- | ------------- |
| Representational State Transfer  | Service Oriented Architecture Protocol  |
| Yaln�zca http protokol� kullan�r  | HTTP, FTP ve SMTP gibi protokolleri kullan�r.  |
| Bir�ok farkl� ver format�n� destekler(JSON,XML,YAML)  | Yaln�zca XML format�n� destekler.  |
| Performance & Scability, Caching  | Performance ve Scability d���kt�r ve bir par�a kar���kt�r.Caching desteklemez. |
| Client ve Server bir Web Environment�inde �al��t�r�ld���nda kullan�l�r.  | Client Server��n �zerindeki objeye eri�meye ihtiya� duydu�unda kullan�l�r.  |

<br>
![MVC - MVVM - MVP](https://i.stack.imgur.com/CFbNC.png)
<br>

# MVC vs MVP vs MVVM

- [ ] MVC
	- [ ] Modal: Kullan�c�ya g�stermek ve manip�le etmesini sa�lamak istedi�imiz verileri i�eren nesnelerdir.
	- [ ] View: Kullan�c�ya Model�i g�sterdi�imiz ve Model �zerinde �e�itli manip�lasyonlara izin verilen yer, UI olarak da nitelendirilebilir.
	- [ ] Controller: Model ve View aras�nda etkile�imi kontrol eder ve View Model�i g�ncellemek(update ) i�in controller�� �a��r�r.Ayr�ca ihtiya� duyulursa birden fazla controller �a��r�labilir.
- [ ] MVP
	- [ ] MVC�ye benzer ama Controller, Presenter ile yer de�i�tirilir.Ancak Presenter, Controller��n aksine g�r�n�m� de�i�tirmekte sorumludur ve View genellikle Presenter�� �a��rmaz.
- [ ] MVVM
	- [ ] Buradaki fark View Model�in varl���d�r.Bir �e�it Observer Design Pattern�dir.�rnek olarak bir slider de��tirilirse yaln�zca Model g�ncellenmez View�da g�r�nt�lenecek veriler de g�ncellenir.Yani iki y�nl� data-binding�e sahiptir.

# Github Merge aras�ndaki fark nelerdir?

![first image](https://i.stack.imgur.com/1bRnI.png)
- [ ] Merge Commit: T�m commitleri feature branch�in ge�mi�inde(history) tutar ve master branch�in i�erisine ta��r.son i�lemde ekstra commit ekleyecektir.
- [ ] Rebase and Merge: Feature brach�in ge�mi�inde ki(history) t�m commitleri master branch�in �n�ne ekler.Son i�lemde ekstra commit eklenmez.
- [ ] Squash and Merge: Feature Brach�in t�m commitlerini tek bir commit�te grupland�racak sonra ana dal�n �n�ne ekleyecektir.Son i�lemde ekstra commit ekleyecektir.
![final image](https://i.stack.imgur.com/hUtiB.png)