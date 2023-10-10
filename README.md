# dotnet_interview
.net interview questions and answers

## Class ve Object Nedir ?
Sınıflar :
  - Verileri ve methodları içine alan kod bloğudur. Sınıflar sayesinde kod yapısı parçalara bölünür ve karmaşıklık azalır.
  - Bir sınıf kendisinde oluşturulacak nesneler için takım üyeler içermelidir.
  - Bu üyeler; alanlar (fields), metodlar (methods), yapıcılar (constructor), özellikler (properties), olaylar (events), delegeler (delegates) olarak sıralanabilir.
  - Örnek: Bir "Araba" sınıfı, arabanın özelliklerini (marka, model, hız) ve davranışlarını (hızlanma, fren yapma) tanımlayabilir.

Nesneler :
  - Sınıflardan üretilirler ve sınıfların aksine kimlikleri vardır.
  - Bir nesne kendi hakkında, yapabileceği işlemler ile ilgili bilgiler saklar. Programın gereksinim duyduğu tüm veriler nesneler tarafıdan tutulur.
  - Örnek: "Araba" sınıfından türetilen bir "Toyota Corolla" nesnesi, belirli bir arabanın özelliklerini ve davranışlarını temsil eder.

## Managed ve Unmanaged Code
Managed Code :
  - CLR (Common Language Runtime) tarafından yürütülen bir koddur. Compiler tarafından derlenmiş koddur.
  - .NET framework tarafından yönetilen ve makine koduna dönüştürülmeden önce ara bir dile çeviren kod bloğududur.
  - Çalışma zamanı (runtime) tarafından otomatik olarak bellek yönetimi, hata denetimi ve güvenlik kontrolleri gibi işlemlerle desteklenir. Bu nedenle, programın daha güvenli ve istikrarlı olmasına yardımcı olur.

Unmanaged Code : 
  - .NET dışındaki herhangi bir framework ile çalışma zamanı tarafından kontrol edilmeyen ve yönetilmeyen kod türünü ifade eder.
  - Genellikle derlenmiş dil (compiled language) veya C/C++ gibi dillerle ilişkilendirilir. Bu tür diller, doğrudan bellek yönetimi ve işletim sistemi kaynaklarına erişim sağlar.

## C# Kod Derleme Aşamaları
İlk adım, C# programınızın kaynak kodunu yazmaktır. Kaynak kod, C# programınızın mantığını ve davranışını tanımlar. Bu kod Visual Studio, Visual Studio Code veya başka bir C# geliştirme ortamında yazılabilir.

Proprocessing :
  - Kaynak kod, önişlem aşamasından geçer. Bu aşamada #include veya #define gibi önişlem direktifleri işlenir.

Compilation :
  - C# kaynak kodunun derlenmesidir. C# derleyicisi bu adımda devreye girer.
  - Derleyici, kaynak kodunuzu alır ve onu çalışabilir bir formata çevirir. Bu aşamada syntax hataları ve mantıksal hatalar tespit edilir.
  - Sonuç olarak, derlenmiş bir program veya kütüphane (genellikle bir .exe veya .dll dosyası) oluşturulur (out generation). Bu derlenmiş kod "Managed Code" olarak adlandırılır.

Linking :
  - Eğer projeniz birden fazla dosya veya modül içeriyorsa, bu aşamada bu dosyalar bir araya getirilir ve bağlanır.
  - Bu, projenin farklı bileşenlerinin birleştirilip bir bütün haline getirilmesini sağlar.
  - Linking işlemi, derlenmiş kodun daha büyük projelerde düzgün çalışabilmesi için önemlidir.

Common Language Runtime :
  - CLR (Common Language Runtime), .NET Framework veya .NET Core gibi platformlarda C# programlarının çalıştırılmasını sağlayan temel bileşendir.
  - CLR, derlenmiş kodu çalıştıran ve yöneten bir çevre sunar. Bu çevre, kodun çalıştırılması, bellek yönetimi, hata yönetimi ve güvenlik kontrolleri gibi işlevleri sağlar.

Execution :
  - CLR tarafından yüklenen derlenmiş kod (Managed Code), runtime sırasında yürütülür.
  - Yani, kullanıcı veya otomatik bir süreç tarafından başlatılan program, CLR içinde çalıştırılır.
  - CLR, programın veri işleme ve kontrol akışını yönetir.

## Temel OOP Kavramları
Kapsülleme :
  - Bir nesnenin bazı özellik ve işlevleri, başka sınıf ve nesnelerden gizlenir.
  - Veri uygulamasının geri kalanı gizlenirken yalnızca gerekli bilgilere erişilebilir.
  - Bu, verilerin doğrudan erişimini engeller ve sınıfın iç mantığına erişimi kontrol eder.

Soyutlama :
  - Bir nesnenin kritik davranışını ve verilerini belirleme ve ilgisiz detayları ortadan kaldırma işlemidir.

Kalıtım :
  - Bir sınıfın başka bir sınıftan özelliklerini ve davranışlarını devralmasını sağlayan bir mekanizmadır.
  - Bu, kodun yeniden kullanılabilirliğini artırır ve sınıflar arasında bir hiyerarşi oluşturabilir.

Polimorfizm :
  - Aynı adı taşıyan metotların farklı sınıflarda farklı şekillerde davranabilmesini ifade eder.
  - Bu, bir arayüzün veya temel sınıfın alt sınıflarında farklı şekillerde uygulanabilmesini sağlar.

## "using" İfade Nedir ?
  - Belirli bir namespace'i içe aktararak (import ederek) o namespace içindeki sınıf ve öğelere daha kolay erişim sağlar.
  - Örneğin, System namespace'ini içe aktararak, Console.WriteLine() gibi System namespace'i içinde tanımlanan sınıf ve metotlara daha kısa bir şekilde erişebilirsiniz.
  - C# projelerinde harici sınıf kütüphanelerini veya assembly'leri kullanmak için using ifadesi kullanılabilir.
  - Bu şekilde, başka bir projede veya pakette bulunan sınıflara erişim sağlanabilir. Özellikle, NuGet paketleri gibi harici kütüphaneler projeye eklenirken using ifadesi kullanılır.

## Regular Expression
  - Regular expression, sayısal ve string ifadenin belirli kurallara uyumluluğunu kontrol etmeye ve düzenlemeye yarar.
  - Regex, dize ayrıştırmanın yanı sıra karakter dizesini değiştirmek için de kullanılır.
  - Metin tabanlı verileri belirli bir desene göre aramak, eşleştirmek ve manipüle etmek için kullanılan güçlü bir metin işleme aracıdır.
  - Regex ifadeleri, metin analizi, metin ayıklama, veri doğrulama, düzenleme ve dönüştürme gibi birçok farklı uygulama alanında kullanılabilir.

## Class vs Struct 
Class :
  - Inheritance destekler.
  - Reference type
  - Üyeleri default olarak private
  - Büyük ve karmaşık modeller için

Struct :
  - Inheritance desteklemez.
  - Value type
  - Üyeleri default olarak public
  - Küçük ve izole modeller için

## Exception Handling
Try - Catch : 
  - Hata Yönetimi, try ve catch blokları aracılığıyla gerçekleştirilir. Kod, try bloğunda çalıştırılır ve eğer bir hata meydana gelirse, bu hata catch bloğunda ele alınır. 

Finally :
  - Bir istisnanın yakalanıp yakalanmadığına bakılmaksızın çalıştırılmak üzere yazılmış bir kod bloğudur.

Throw :
  - Bir sorun oluştuğunda bir istisna atar.

## Constructor ve Destructor Kavramları
Constructor(Yapıcı Metot) :
  - Bir sınıfın bir nesnesi (instance) oluşturulduğunda otomatik olarak çalışan özel bir metottur.
  - Constructor, sınıf adı ile aynı isimde olmalıdır.
  - Parametre alabilir veya parametresiz olabilir. Overload edilebilir. Geriye değer döndürmezler. 

  ```
      class Person
    {
        public string Name;
        public int Age;
    
        // Parametresiz constructor
        public Person()
        {
            Name = "Unknown";
            Age = 0;
        }
    
        // Parametre alan constructor
        public Person(string name, int age)
        {
            Name = name;
            Age = age;
        }

        // Destructor tanımı
        ~PersonDestructor()
        {
            // Nesne yıkıldığında buraya gelinir
            // Kaynakları serbest bırakmak için kullanılabilir
        }
    }
    
    // Nesne oluşturma ve constructor kullanımı
    Person person1 = new Person(); // Parametresiz constructor
    Person person2 = new Person("Alice", 30); // Parametre alan constructor

  ```

Destructor(Yıkıcı Metot) :
  - Bir nesne ömrü sona erdiğinde (garbage collector tarafından toplandığında) otomatik olarak çalışan metottur.
  - C# programlama dilinde, ~ (tilde) işareti ile başlayan bir metot adı ile tanımlanır.
  - Genellikle unmanaged kaynakları (bellek, dosya işlemleri, bağlantılar vb.) serbest bırakmak için kullanılır.
  - C# programcıları genellikle Destructorları özel olarak tanımlamak zorunda kalmazlar, çünkü çoğu zaman .NET çöp toplayıcı (garbage collector) bu kaynakları yönetir.













