# REST vs SOAP

| REST  | SOAP |
| ------------- | ------------- |
| Representational State Transfer  | Service Oriented Architecture Protocol  |
| Yalnýzca http protokolü kullanýr  | HTTP, FTP ve SMTP gibi protokolleri kullanýr.  |
| Birçok farklý ver formatýný destekler(JSON,XML,YAML)  | Yalnýzca XML formatýný destekler.  |
| Performance & Scability, Caching  | Performance ve Scability düþüktür ve bir parça karýþýktýr.Caching desteklemez. |
| Client ve Server bir Web Environment’inde çalýþtýrýldýðýnda kullanýlýr.  | Client Server’ýn üzerindeki objeye eriþmeye ihtiyaþ duyduðunda kullanýlýr.  |

<br>
![MVC - MVVM - MVP](https://i.stack.imgur.com/CFbNC.png)
<br>

# MVC vs MVP vs MVVM

- [ ] MVC
	- [ ] Modal: Kullanýcýya göstermek ve manipüle etmesini saðlamak istediðimiz verileri içeren nesnelerdir.
	- [ ] View: Kullanýcýya Model’i gösterdiðimiz ve Model üzerinde çeþitli manipülasyonlara izin verilen yer, UI olarak da nitelendirilebilir.
	- [ ] Controller: Model ve View arasýnda etkileþimi kontrol eder ve View Model’i güncellemek(update ) için controller’ý çaðýrýr.Ayrýca ihtiyaç duyulursa birden fazla controller çaðýrýlabilir.
- [ ] MVP
	- [ ] MVC’ye benzer ama Controller, Presenter ile yer deðiþtirilir.Ancak Presenter, Controller’ýn aksine görünümü deðiþtirmekte sorumludur ve View genellikle Presenter’ý çaðýrmaz.
- [ ] MVVM
	- [ ] Buradaki fark View Model’in varlýðýdýr.Bir çeþit Observer Design Pattern’dir.Örnek olarak bir slider deðþtirilirse yalnýzca Model güncellenmez View’da görüntülenecek veriler de güncellenir.Yani iki yönlü data-binding’e sahiptir.

# Github Merge arasýndaki fark nelerdir?

![first image](https://i.stack.imgur.com/1bRnI.png)
- [ ] Merge Commit: Tüm commitleri feature branch’in geçmiþinde(history) tutar ve master branch’in içerisine taþýr.son iþlemde ekstra commit ekleyecektir.
- [ ] Rebase and Merge: Feature brach’in geçmiþinde ki(history) tüm commitleri master branch’in önüne ekler.Son iþlemde ekstra commit eklenmez.
- [ ] Squash and Merge: Feature Brach’in tüm commitlerini tek bir commit’te gruplandýracak sonra ana dalýn önüne ekleyecektir.Son iþlemde ekstra commit ekleyecektir.
![final image](https://i.stack.imgur.com/hUtiB.png)