# 091258129131-83_wahyu_nurcahyo_mongodts_pro_2021_doc.js
PRACTICAL EXAM MONGODTS PRO 2021

/*
** Dibuat oleh: Wahyu Nurcahyo
** No. Peserta: 131-83
*/

/*
**[PRAKTIK - 01] | Urutan perintah yang dilakukan untuk membuat database marketdb dan dengan nama collection-nya products adalah....
*/
> use marketdb
switched to db marketdb
> db.createCollection("products")
{ "ok" : 1 }


/*
**[PRAKTIK - 02] | Manakah dari perintah berikut yang akan berhasil memasukkan 3 dokumen baru ke dalam koleksi products yang kosong?
*/
> db.products.insertMany([
... {_id: 1, name: "Indomie Goreng"},
... {_id: 2, name: "Indomie Kuah"},
... {_id: 3, name: "Sarimie"}
... ])


/*
**[PRAKTIK - 03] | Urutan perintah yang digunakan untuk menghapus collection products pada database marketdb saat pertama kali membuka mongoshell adalah.... 
*/
> use marketdb
switched to db marketdb
> db.products.drop()
true


/*
**[PRAKTIK - 04] | Jalankan perintah insertMany dari script ini: https://gist.github.com/joesoeph/7f1dfded51db1d08afe2bdff4e43a831. Gunakan perintah itu untuk insert dokumen pada collection products yang ada di database marketdb. Setelah melakukan insert, berapa dokumen yang berhasil tersimpan? 
*/
db.products.insertMany([
...   {
...     _id: 1,
...     name: "Indomie Ayam Bawang",
...     price: 3000,
...     stock: 30,
...     unit: "pcs",
...     description: "Harga jual perbungkus",
...     categories: ["makanan", "mie"],
...     suppliers: [
...       {
...         name: "Oemah Mie",
...         city: "DKI Jakarta"
...       },
...       {
...         name: "Gudang Mie",
...         city: "Bandung"
...       }
...     ],
...     expired_at: new Date("2022-01-01"),
...     created_at: new Date("2021-01-01")
...   },
...   {
...     _id: 2,
...     name: "Mie Sedap Goreng",
...     price: 2500,
...     stock: 10,
...     unit: "pcs",
...     description: "Harga jual perbungkus",
...     categories: ["makanan", "mie"],
...     suppliers: [
...       {
...         name: "Mie-ku",
...         city: "DKI Jakarta"
...       },
...       {
...         name: "Rumah Mie",
...         city: "Bandung"
...       }
...     ],
...     expired_at: new Date("2022-02-01"),
...     created_at: new Date("2021-01-02")
...   },
...   {
...     _id: 3,
...     name: "Indomie Goreng",
...     price: 3000,
...     stock: 15,
...     unit: "pcs",
...     description: "Harga jual perbungkus",
...     categories: ["makanan", "mie"],
...     suppliers: [
...       {
...         name: "Oemah Mie",
...         city: "DKI Jakarta"
...       },
...       {
...         name: "Gudang Mie",
...         city: "Bandung"
...       }
...     ],
...     expired_at: new Date("2022-02-01"),
...     created_at: new Date("2021-01-02")
...   },
...   {
...     _id: 4,
...     name: "Indomie Soto Lamongan",
...     price: 3000,
...     stock: 30,
...     unit: "pcs",
...     description: "Harga jual perbungkus",
...     categories: ["makanan", "mie"],
...     suppliers: [
...       {
...         name: "Oemah Mie",
...         city: "DKI Jakarta"
...       },
...       {
...         name: "Gudang Mie",
...         city: "Bandung"
...       }
...     ],
...     expired_at: new Date("2022-03-01"),
...     created_at: new Date("2021-02-01")
...   },
...   {
...     _id: 5,
...     name: "Sarimie Ayam Penyet",
...     price: 1500,
...     stock: 50,
...     unit: "pcs",
...     description: "Harga jual perbungkus",
...     categories: ["makanan", "mie"],
...     expired_at: new Date("2022-03-01"),
...     created_at: new Date("2021-02-01")
...   },
...   {
...     _id: 6,
...     name: "Alpukat Mentega",
...     price: 20000,
...     stock: 90.4,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah"],
...     suppliers: [
...       {
...         name: "Pasar Induk",
...         city: "DKI Jakarta"
...       }
...     ],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 7,
...     name: "Mangga",
...     price: 15000,
...     stock: 180.9,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah"],
...     suppliers: [
...       {
...         name: "Pasar Induk",
...         city: "DKI Jakarta"
...       },
...       {
...         name: "Pasar Kecapi",
...         city: "Bekasi"
...       }
...     ],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 8,
...     name: "Buah Naga",
...     price: 12000,
...     stock: 30.2,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah"],
...     suppliers: [
...       {
...         name: "Gudang Buah & Sayur",
...         city: "Semarang"
...       },
...       {
...         name: "Pasar Kecapi",
...         city: "Bekasi"
...       }
...     ],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 9,
...     name: "Anggur",
...     price: 35000,
...     stock: 30.5,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah"],
...     suppliers: [
...       {
...         name: "Gudang Buah & Sayur",
...         city: "Semarang"
...       },
...       {
...         name: "Pasar Kecapi",
...         city: "Bekasi"
...       }
...     ],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 10,
...     name: "Semangka",
...     price: 30000,
...     stock: 500.2,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah"],
...     suppliers: [
...       {
...         name: "Pasar Induk",
...         city: "Semarang"
...       },
...       {
...         name: "Pasar Kecapi",
...         city: "Bekasi"
...       }
...     ],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 0,
...     name: "Kopi",
...     price: 150000,
...     stock: 500.2,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah"],
...     suppliers: [
...       {
...         name: "Antar Kopi",
...         city: "Aceh"
...       }
...     ],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 11,
...     name: "Cabai",
...     price: 100000,
...     stock: 100,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah", "sayur"],
...     suppliers: [
...       {
...         name: "Pasar Induk",
...         city: "DKI Jakarta"
...       },
...       {
...         name: "Pasar Kecapi",
...         city: "Bekasi"
...       }
...     ],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 12,
...     name: "Tomat",
...     price: 10000,
...     stock: 100,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "buah", "sayur"],
...     created_at: new Date("2021-03-01")
...   },
...   {
...     _id: 13,
...     name: "Beras",
...     price: 14000,
...     stock: 100,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "sembako"],
...     suppliers: [
...       {
...         name: "Pasar Induk",
...         city: "DKI Jakarta"
...       },
...       {
...         name: "Pasar Kecapi",
...         city: "Bekasi"
...       }
...     ],
...     created_at: new Date("2021-03-03")
...   },
...   {
...     _id: 14,
...     name: "Minyak Goreng",
...     price: 12000,
...     stock: 55.5,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "sembako"],
...     created_at: new Date("2021-03-03")
...   },
...   {
...     _id: 15,
...     name: "Gula",
...     price: 31000,
...     stock: 120.5,
...     unit: "kg",
...     description: "Harga jual per kilo, stock dalam kilo",
...     categories: ["makanan", "sembako"],
...     created_at: new Date("2021-03-03")
...   }
... ])
{
        "acknowledged" : true,
        "insertedIds" : [
                1,
                2,
                3,
                4,
                5,
                6,
                7,
                8,
                9,
                10,
                0,
                11,
                12,
                13,
                14,
                15
        ]
}


/*
**[PRAKTIK - 05] | Berdasarkan praktik 04, berapa nilai _id yang terbesar? 
*/
15

/*
**[PRAKTIK - 06] | Perintah query untuk mencari produk yang stock nya tidak lebih dari 50 dan salah satu suppliers nya ada yang beralamat di kota Bandung adalah
*/
> db.products.find()({
... stock: { $lte: 50},
... suppliers: {$elemMatch: {city: "Bandung"}}
... })
uncaught exception: TypeError: db.products.find(...) is not a function :
@(shell):1:1
> db.products.find({ stock: { $lte: 50}, suppliers: {$elemMatch: {city: "Bandung"}} })
{ "_id" : 1, "name" : "Indomie Ayam Bawang", "price" : 3000, "stock" : 30, "unit" : "pcs", "description" : "Harga jual perbungkus", "categories" : [ "makanan", "mie" ], "suppliers" : [ { "name" : "Oemah Mie", "city" : "DKI Jakarta" }, { "name" : "Gudang Mie", "city" : "Bandung" } ], "expired_at" : ISODate("2022-01-01T00:00:00Z"), "created_at" : ISODate("2021-01-01T00:00:00Z") }
{ "_id" : 2, "name" : "Mie Sedap Goreng", "price" : 2500, "stock" : 10, "unit" : "pcs", "description" : "Harga jual perbungkus", "categories" : [ "makanan", "mie" ], "suppliers" : [ { "name" : "Mie-ku", "city" : "DKI Jakarta" }, { "name" : "Rumah Mie", "city" : "Bandung" } ], "expired_at" : ISODate("2022-02-01T00:00:00Z"), "created_at" : ISODate("2021-01-02T00:00:00Z") }
{ "_id" : 3, "name" : "Indomie Goreng", "price" : 3000, "stock" : 15, "unit" : "pcs", "description" : "Harga jual perbungkus", "categories" : [ "makanan", "mie" ], "suppliers" : [ { "name" : "Oemah Mie", "city" : "DKI Jakarta" }, { "name" : "Gudang Mie", "city" : "Bandung" } ], "expired_at" : ISODate("2022-02-01T00:00:00Z"), "created_at" : ISODate("2021-01-02T00:00:00Z") }
{ "_id" : 4, "name" : "Indomie Soto Lamongan", "price" : 3000, "stock" : 30, "unit" : "pcs", "description" : "Harga jual perbungkus", "categories" : [ "makanan", "mie" ], "suppliers" : [ { "name" : "Oemah Mie", "city" : "DKI Jakarta" }, { "name" : "Gudang Mie", "city" : "Bandung" } ], "expired_at" : ISODate("2022-03-01T00:00:00Z"), "created_at" : ISODate("2021-02-01T00:00:00Z") }


/*
**[PRAKTIK - 07] | Perintah query untuk menampilkan dokumen yang tidak memiliki field suppliers adalah....
*/
> db.products.find({
... suppliers: { $exists: false }
... })


/*
**[PRAKTIK - 08] | Dari soal [PRAKTIK - 06], perintah query untuk menampilkan dokumen hanya field name, price, stock, dan unit nya saja adalah...
*/
> db.products.find( { stock: { $lte: 50}, suppliers: { $elemMatch: {city: "Bandung"} } }, { _id: 0, name: 1, price: 1, stock: 1, unit: 1 })
{ "name" : "Indomie Ayam Bawang", "price" : 3000, "stock" : 30, "unit" : "pcs" }
{ "name" : "Mie Sedap Goreng", "price" : 2500, "stock" : 10, "unit" : "pcs" }
{ "name" : "Indomie Goreng", "price" : 3000, "stock" : 15, "unit" : "pcs" }
{ "name" : "Indomie Soto Lamongan", "price" : 3000, "stock" : 30, "unit" : "pcs" }


/*
**[PRAKTIK - 09] | Perintah query untuk menampilkan total dokumen yang memiliki field suppliers adalah...
*/
 db.products.find({
... suppliers: { $exists: true }
... }).count()


/*
**[PRAKTIK - 10] | Perintah yang digunakan untuk menampilkan 5 dokumen products, yang memiliki stock terbanyak adalah..
*/
> db.products.find().sort({ stock: -1}).limit(5)
> > db.products.find().limit(5).sort({ stock: -1 })


/*
**[PRAKTIK - 11] | Perintah untuk melakukan insert dokumen baru dengan ketentuan field seperti gambar ini adalah....
*/
> db.products.insertOne({
... _id: 16,
... name: "Paramex",
... stock: "30",
... unit: "strip"
... })


/*
**[PRAKTIK - 12] | Lanjutan dari [PRAKTIK - 11], perintah yang digunakan untuk melakukan update dokumen yang field id adalah 16 dengan hasil akhir sesuai gambar ini adalah..
*/
> db.products.replaceOne({
... id: 16
... },{
... _id: 16,
... name: "Paramex",
... stock: 30,
... unit: "strip",
... categories: ["kimia", "obat"]
... })


/*
**[PRAKTIK - 13] | Perintah yang digunakan untuk menambahkan field description dengan value "Harga jual per strip, stok dalam strip" pada dokumen dengan id 16 adalah...
*/
> db.products.updateOne({ _id: 16 }, { $set: { description: "Harga jual per strip, stok dalam strip" } })


/*
**[PRAKTIK - 14] | Urutan perintah yang digunakan untuk menghapus collection product pada database marketdb saat pertama kali menjalankan mongoshell adalah..
*/
> use marketdb
switched to db marketdb
> db.products.drop()


/*
**[PRAKTIK - 15] | Masukkan perintah untuk mengecek berapa jumlah collection pada database marketdb yang sudah kamu buat selama menyelesaikan soal sebelumnya. Berapa jumlah collection yang kamu miliki?
*/
> db.getCollectionNames()
[ ]
