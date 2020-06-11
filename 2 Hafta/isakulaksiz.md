# REST vs SOAP	

| REST  | SOAP |	
| ------------- | ------------- |	
| Representational State Transfer  | Service Oriented Architecture Protocol  |	
| Yalnızca http protokolü kullanır  | HTTP, FTP ve SMTP gibi protokolleri kullanır.  |	
| Birçok farklı ver formatını destekler(JSON,XML,YAML)  | Yalnızca XML formatını destekler.  |	
| Performance & Scability, Caching  | Performance ve Scability düşüktür ve bir parça karışıktır.Caching desteklemez. |	
| Client ve Server bir Web Environment’inde çalıştırıldığında kullanılır.  | Client Server’ın üzerindeki objeye erişmeye ihtiyaş duyduğunda kullanılır.  |	

<br>	
# MVC vs MVP vs MVVM	

- [ ] MVC	
	- [ ] Modal: Kullanıcıya göstermek ve manipüle etmesini sağlamak istediğimiz verileri içeren nesnelerdir.	
	- [ ] View: Kullanıcıya Model’i gösterdiğimiz ve Model üzerinde çeşitli manipülasyonlara izin verilen yer, UI olarak da nitelendirilebilir.	
	- [ ] Controller: Model ve View arasında etkileşimi kontrol eder ve View Model’i güncellemek(update ) için controller’ı çağırır.Ayrıca ihtiyaç duyulursa birden fazla controller çağırılabilir.	
- [ ] MVP	
	- [ ] MVC’ye benzer ama Controller, Presenter ile yer değiştirilir.Ancak Presenter, Controller’ın aksine görünümü değiştirmekte sorumludur ve View genellikle Presenter’ı çağırmaz.	
- [ ] MVVM	
	- [ ] Buradaki fark View Model’in varlığıdır.Bir çeşit Observer Design Pattern’dir.Örnek olarak bir slider değştirilirse yalnızca Model güncellenmez View’da görüntülenecek veriler de güncellenir.Yani iki yönlü data-binding’e sahiptir.	

# Github Merge arasındaki fark nelerdir?	

![first image](https://i.stack.imgur.com/1bRnI.png)	
- [ ] Merge Commit: Tüm commitleri feature branch’in geçmişinde(history) tutar ve master branch’in içerisine taşır.son işlemde ekstra commit ekleyecektir.	
- [ ] Rebase and Merge: Feature brach’in geçmişinde ki(history) tüm commitleri master branch’in önüne ekler.Son işlemde ekstra commit eklenmez.	
- [ ] Squash and Merge: Feature Brach’in tüm commitlerini tek bir commit’te gruplandıracak sonra ana dalın önüne ekleyecektir.Son işlemde ekstra commit ekleyecektir.	
![final image](https://i.stack.imgur.com/hUtiB.png)
