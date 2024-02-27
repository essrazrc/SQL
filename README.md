# SQL
SQL İLE TABLO OLUŞTURMA VE İŞLEM YAPMA
//KOMUT KULLANARAK TABLO OLUSTURMA//

create table ogrenci(
ogrenciNo int not null primary key,
ad varchar(40) not null,
soyad varchar(50) not null,
dogumYili int not null,
bolum varchar(100)
);


//tablo silme//
drop table ogrenci


//tabloya ekleme yapmak icin//
insert into ogrenci values(1,'esra','zaric',2003,NULL);
insert into ogrenci(ogrenciNo,ad,soyad,dogumYili) values(2,'ayse','kaya',1999);
insert into ogrenci values(3,'okan','yılmaz',1987,'yazilim mühendisligi');
insert into ogrenci values(4,'ali','kaya',1974,'yazilim mühendisligi');

//tabloda veri güncellemesi yapmak icin//
update ogrenci set ad='akın' where bolum='yazilim mühendisligi'
update ogrenci set bolum='bilgisayar müh' where ad='esra'
update ogrenci set bolum='elektrik' where bolum='yazilim mühendisligi'

//istedigimiz veriyi ekrana yazdırma//
select *from ogrenci where ad='esra'
select *from ogrenci where bolum='yazilim mühendisligi'

//alfabetik sıralama//
select *from ogrenci order by ad asc
select *from ogrenci order by soyad asc

//ters alfabetik sıralama//
select *from ogrenci order by ad desc
select *from ogrenci order by soyad desc

//once ad a gore sonra soyada göre alfabetik sıralama//
select *from ogrenci order by ad,soyad

//between kullanımı//
select *from ogrenci where dogumYili between 1980 and 2000 order by ad


