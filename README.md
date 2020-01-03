# restapi-cekresi
RESTful API untuk mengecek status pengiriman, ongkos kirim dan kebutuhan lainnya diberbagai jasa ekspedisi domestik dan internasional.

### Province
> Method "province" digunakan untuk mendapatkan daftar propinsi yang ada di Indonesia.

Method 	| URL
------- | ---------
GET 	| https://api.econxn.id/v1/couriers/province/


Parameter | Wajib | Tipe | Keterangan
------ | ------ | ------ | ------
id | Tidak | String | ID provinsi

PHP Request:
```<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.econxn.id/v1/couriers/province/?id=2",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET"
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

