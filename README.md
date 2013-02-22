# Django Sprint Kılavuzu

## Geliştirme Ortamının Kurulması

Katılımcılardan, etkinliğe gelmeden önce geliştirme ortamlarını hazır
etmelerini bekliyoruz. Etkinlik süresince bunun için ayrı zaman
ayrılmayacaktır.

Öncelikle GitHub üzerinde [Django kaynak kodunu][dj-gh] forklayıp geliştirmeye
başlayabilirsiniz.

* Eğer Vagrant'a aşinaysanız; üzerinde çalışacağınız ticketlar birden fazla
  Django sürümünü kapsıyorsa veya ORM gibi birden fazla veritabanı kurulumu
  gerektiren bir ticket üzerinde çalışıyorsanız [djangocore-box][dj-box]'u
  kullanabilirsiniz.

[dj-gh]: https://github.com/django/django
[dj-box]: https://github.com/jphalip/djangocore-box

* Eğer Mac fanboyu değilseniz elle kurulum için tek ihtiyacınız
  [Virtualenv][dj-venv]:

  ```sh
  $ git clone git@github.com:<KULLANICI_ADINIZ>/django.git
  $ cd django
  $ # 1.7+ sürümlerde --no-site-packages opsiyonunu kullanmanıza gerek yok
  $ virtualenv venv
  $ source venv/bin/activate.sh
  ```

[dj-venv]: http://www.virtualenv.org/

* [Virtualenvwrapper][dj-vw]'ı kullanırsanız hayatınız daha da kolaylaşabilir:

  ```sh
  $ git clone git@github.com:<KULLANICI_ADINIZ>/django.git
  $ mkvirtualenv djangosprint
  ```

  Sanal geliştirme ortamından çıkmak için `deactivate`, mevcut geliştirme
  ortamlarını listelemek için `workon`, `mkvirtualenv` ile oluşturduğunuz bir
  geliştirme ortamına geçmek içinse `workon <geliştirme ortamının adı>`
  komutlarını verebilirsiniz.

[dj-vw]: http://virtualenvwrapper.readthedocs.org/en/latest/

* Gerek virtualenv, gerekse virtualenvwrapper kullandığınız çözümlerde

  ```sh
  $ pip install -e <django_dizini>
  ```

  komutu ile lokalinizdeki Django kodunu sanal geliştirme ortamınızda
  kullanmaya başlayabilirsiniz.


## Geliştirmeye başlamadan önce

1. Daha önce bir açık kaynak projenin geliştirilmesinde görev almadıysanız ya
   da Django'nun geliştirme sürecine yabancıysanız öncelikle
   [Advice for new contributors][dj-newbie] belgesini okuyun.

### Önemli Bağlantılar

* [Django kaynak kodu](https://github.com/django/django)
* [Django tracker](https://code.djangoproject.com/query)

[dj-newbie]: https://docs.djangoproject.com/en/dev/internals/contributing/new-contributors/


## Workflow

**Not:** Bu belgede listelenen ticketlardan biri üzerinde çalışmak zorunda
değilsiniz ancak ne üzerinde çalıştığınızı [İş Bölümü][dj-is] sayfasına
eklemeninizi bekliyoruz.

1. Çalışmak istediğiniz bir ya da birden fazla ticket'ın numarasını Wiki'deki
   [İş Bölümü][dj-is] sayfasında yazmanız birden fazla kişinin aynı ticket
   üzerinde çalışmasını engellemek adına faydalı olacaktır.

[dj-is]: https://github.com/pyistanbul/sprints/wiki/%C4%B0%C5%9F-B%C3%B6l%C3%BCm%C3%BC


## Ticketlar

* https://code.djangoproject.com/ticket/16134

### Eklenebilecek Fikirler

Django tracker'ında bulunmayan herhangi bir fikriniz varsa ya da boş zamanı
olan başka bir katılımcının üzerinde çalışmasını istiyorsanız
[Fikirler][dj-ideas] sayfasına ekleyebilirsiniz.

[dj-ideas]: https://github.com/pyistanbul/sprints/wiki/Fikirler

### Faydalı Trac Sorguları

* [Eklenecek]


## İletişim

Türkçe iletişim için Freenode üzerindeki `#pyistanbul`, resmi ve İngilizce
iletişim için ise yine Freenode üzerindeki `#django-sprint` kanalını
kullanabilirsiniz.
