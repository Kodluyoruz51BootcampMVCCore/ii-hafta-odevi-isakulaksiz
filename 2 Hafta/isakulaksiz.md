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

# Git-flow

![first image](https://miro.medium.com/max/638/0*PRJYeVCeztuOuddN.jpg)
- [ ] Develop: bir sonraki sürüm için yapılan değişiklikler güncellenir.Ayrıca Jenkins ile CI aracına bağlanarak sürekli inşa edilebilir.
- [ ] Master: production ready(yayına alınabilir) kod bulunur.
- [ ] Feature: Yeni özellik ekleneceği zaman bu özellik feature dalına eklenir.Buradaki özellikten kasıt birden fazla commit içeren büyük değişiklikler diyebiliriz.
- [ ] Release: Sürümdeki sonn değişiklikler(sürüm numarası) bu dalda yapılır.
- [ ] Hotfix: Sürümde kritik bir hata keşfedilmesi durumunda hatanın çözülüp yayına alınmasında hotfix dalı kullanılır.

# pull request vs issue
- [ ] öncelikle bir dosyayı pull request olarak göndermek demek projede değişiklikler yaptım sen de bu değişiklikleri onayla ve merge et bende katkı sağlamış olayım anlamına gelir.
- [ ] issue ise yapılacak işleri, sorunları kaydedebileceğimiz ve listeleyebileceğimiz bir ekrandır.Issue projenin hatalarını izlemek için harika bir yoldur.
- [ ] Gelelim neden id’lerin artma sebebine, pull request’de id’nin yanında branch ismi yer alır yapılan değişikliklerde id değerinin arttığını gözlemleyebiliriz.

# ASP.NET Boilerplate, ABP Framework
- [ ] .NET Core için hazırlanmıi open source bir web application frameworkleridir
- [ ] ABP framework by Volosoft
- [ ] ABP modern web uygulamaları için full stack geliştirme sağlayan bir platformdur.Böylece gelişitricinin üretkenliğini artırmada yardımcı olmaktadır.Sahip olduğu özellikler :
	- [ ] Modular, Layered Architecture based on Domain Driven Design
	- [ ] Microservice Focused
	- [ ] Multi-Tenancy
	- [ ] Virtual File System & Theming
	- [ ] Free & Open Source (LGPL licensed)

# Serialize vs Deserialize
- [ ] Serialize: nesne runtimedaki durumlarını alıp bir kaynağa transfer etmek için bir formata dönüştürülüp yazma işlemine denir.
- [ ] Deserialize: Bir kaynakta (file,db) bulunan serileştirilmiş bir formattaki nesnelerin ihtiyaç olduğu durumlarda run timedaki durumuna dönüştürülme işlemidir. 
	- [ ] Binary Serialization : Binary serileştirme için gerekli olan sınıflar System.Runtime.Serialization.Formatters.Binary altında bulunmaktadır.Nesneler byte array şekline dönüştürülür.
```
public static byte[] BinarySerialize(object graph)
{
    using (var stream = new MemoryStream())
    {
        var formatter = new BinaryFormatter();
 
        formatter.Serialize(stream, graph);
 
        return stream.ToArray();
    }
}

```
	- [ ] SOAP Serialization: Bir nesnenin SOAP protokolü üzerinden transfer edilebilmesi için bu formata uygun serileştirilebilmesi işlemidir.Gerekli olan sınıflar System.Runtime.Serialization.Formatters.SOAP altında yer almaktadır.
```
public static string SoapSerialize(object graph)
{
   using (var stream = new MemoryStream())
   {
      var formatter = new SoapFormatter();
 
      formatter.Serialize(stream, graph);
 
      return Encoding.UTF8.GetString(
                stream.GetBuffer(), 0, (int)stream.Position);
   }
}
```
	- [ ] JSON Serialization: Nesneleri JSON şeklinde serileştirilmesine denir.Burada Json.Net kütüphanesi kullanılabilir.
```
public static string JsonSerialize(object graph)
{
    return JsonConvert.SerializeObject(graph);
}
```

# Console Application vs IIS
![first image]( https://docs.microsoft.com/tr-tr/aspnet/core/host-and-deploy/iis/index/_static/ancm-inprocess.png?view=aspnetcore-3.1)
- [ ] IIS temelde local bilgisayarımızı bir web server olarak kullanabileceğimiz bir sistemdir.
- [ ] İstekler Web’den çekirdek modu http.sys sürücüsüne ulaşır.
- [ ] Sürücü, Web sitesinin yapılandırılmış bağlantı noktasında istekleri IIS’e yönlendirir.Yapılandırılmış bağlantı noktası genellikle 80 (HTTP) veya 443 (HTTPS)
- [ ] Modül, isteği uygulama için rastgele bir bağlantı noktasında Kestrel’e iletir.Rastgele bağlantı noktası 80 veya 443 değildir.

# Razor Nedir?
- [ ] ASP.NET teknolojisinde C# ie birlikte dinamik sayfalar oluşturmaya yarayan bir söz dizimidir.Razor syntax aracılığıyla ana makine kısmında(server side) çalışacak kodların ayrımını @ işareti aracılığıyla yapılmaktadır.Ayrıca Frontend çatılarında kullanılan MVVM yapısına benzeyen two way binding özelliğini desteklemektedir.
- [ ] @page dosyayı MVC’ye dönüştürür.Bu bir denetleyiciden geçmeden istekleri doğrudan işlediği anlamına gelir
