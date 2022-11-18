## Karyawan
<details>
<summary> Klik untuk Ekspan </summary>

### Create karyawan
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/karyawan </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "Sri Meiylani Rejeki",
    "alamat" : "Ciawi",
    "hobi" : "Memasak"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data karyawan Berhasil diinput",
    "data" : {
        "id" : 1234,
        "nama" : "Sri Meiylani Rejeki",
        "alamat" : "Ciawi",
        "hobi" : "Memasak"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama karyawan Telah digunakan",
    "data" : {
        "value" : "Sri Meiylani Rejeki",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read karyawan By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/karyawan </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/karyawan?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : 000112,
        "nama" : "Sri Meiylani Rejeki",
        "alamat" : "Ciawi",
        "hobi" : "Memasak"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID karyawan tidak ditemukan",
    "data" : {
        "value" : 1234,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read karyawan All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/karyawan </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "id" : 000112,
            "nama" : "Sri Meiylani Rejeki",
            "alamat" : "Ciawi",
            "hobi" : "Memasak"
        },
        {
            "id" : 000113,
            "nama" : "Sri Mulyani Rahayu",
            "alamat" : "Bogor",
            "hobi" : "Menari dan Menyanyi"
        },
        {
            "id" : 000113,
            "nama" : "Sri Mulyati lestari",
            "alamat" : "Ciawi",
            "hobi" : "Olahraga"
        }

    ]
}    
```

</td>
</tr>
</table>

### Update karyawan
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/karyawan </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : 000112,
    "nama" : "Sri Meiylani Rejeki",
    "alamat" : "Jalan Raya Ciawi Tipar 04/04 Ciawi Bogor",
    "hobi" : "Olahraga dan Memasak"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data karyawan Berhasil diubah",
    "data" : {
         "id" : 000112,
        "nama" : "Sri Meiylani Rejeki",
        "alamat" : "Jalan Raya Ciawi Tipar 04/04 Ciawi Bogor",
        "hobi" : "Olahraga dan Memasak"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama karyawan Telah digunakan",
    "data" : {
        "value" : "Sri Meiylani Rejeki",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID karyawan tidak ditemukan",
    "data" : {
        "value" : 000112,
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete karyawan
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/karyawan </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/karyawan?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : [] 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID karyawan tidak ditemukan",
    "data" : {
        "value" : 000112,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>