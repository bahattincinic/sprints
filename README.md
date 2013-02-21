# Django Sprint Kılavuzu

## Geliştirme Ortamının Kurulması

Katılımcılardan, etkinliğe gelmeden önce geliştirme ortamlarını hazır etmelerini bekliyoruz. Etkinlik süresince bunun için ayrı zaman ayrılmayacaktır.

Öncelikle github hesabınıza django kaynak kodunu forklayıp geliştirmeye başlayabilirsiniz. Bu sayede yaptığınız değişiklikler için pull request göndermeniz daha kolay olacaktır.

* Eğer Vagrant'a aşinaysanız ve üzerinde çalışacağınız ticketlar birden fazla Django sürümünü kapsıyorsa,
*djangocore-box*'u kullanabilirsiniz: https://github.com/jphalip/djangocore-box

* Eğer Mac fanboyu değilseniz elle kurulum için tek ihtiyacınız Virtualenv:

```sh
$ git clone git@github.com:<KULLANICI_ADINIZ>/django.git
$ cd django
$ virtualenv venv  # 1.7 ve üzeri sürümlerde --no-site-packages opsiyonunu kullanmanıza gerek yok
$ source venv/bin/activate.sh
```
* Virtualenvwrapper'ı kullanırsanız hayatınız daha da kolaylaşabilir:

```sh
$ git clone git@github.com:<KULLANICI_ADINIZ>/django.git
$ mkvirtualenv djangosprint
```
Sanal geliştirme ortamından çıkmak için *deactivate*, mevcut geliştirme ortamlarını listelemek için *workon*, "mkvirtualenv" ile oluşturduğunuz bir geliştirme ortamına geçmek içinse *workon <geliştirme ortamının adı>* komutlarını verebilirsiniz.

* Gerek virtualenv, gerekse virtualenvwrapper kullandığınız çözümlerde 

```sh
$ pip install -e <django_dizini>
```
komutu ile lokalinizdeki django kodunu sanal geliştirme ortamınızda kullanmaya başlayabilirsiniz.

## Geliştirmeye başlamadan önce

1. Nereden başlayacağınızı bilmiyorsanız öncelikle [Advice for new contributors](https://docs.djangoproject.com/en/dev/internals/contributing/new-contributors/) dökümanını okuyun.

## Workflow

1. *Ticketlar* başlığından çalışmak istediğiniz bir ya da birden fazla ticket'ın numarasını Wiki'deki
   [İş Bölümü](https://github.com/pyistanbul/sprints/wiki/%C4%B0%C5%9F-B%C3%B6l%C3%BCm%C3%BC)
   sayfasında yazmanız birden fazla kişinin aynı ticket üzerinde çalışmasını engellemek adına faydalı
   olacaktır.

## Ticketlar

* https://code.djangoproject.com/ticket/16134

### Faydalı Track sorguları

* [TBA]

## Eklenebilecek Fikirler

**Not:** Aşağıdaki maddelerle alakalı Django tracker'ında daha önce bir ticket açılmış olabilir.
Üzerinde çalışmaya başlamadan önce, tracker'da arama yapıp, eğer ilgili bir ticket bulamadıysanız
açmanız gerekiyor.

### Django Belgeleri

* "Making queries" belgelerinde her karşılaştırma operatörünün örneği yok:
  https://docs.djangoproject.com/en/dev/topics/db/queries/#retrieving-specific-objects-with-filters

  Mesela "in" için arama yapılmak istenildiğinde ancak StackOverflow'dan görebiliyorsunuz:
  http://stackoverflow.com/questions/5481890/django-does-the-orm-support-the-sql-in-operator

  Django kullanıcıları için belki çok büyük bir eksik değil ama bir şekilde koda dokunması
  gerekenler veya Django'ya yeni başlayanlar için referans niyetine bir liste eklemek güzel olabilir.

## İletişim

Türkçe iletişim için Freenode üzerindeki `#pyistanbul`, resmi ve İngilizce iletişim için ise yine
Freenode üzerindeki `#django-sprint` kanalını kullanabilirsiniz.
