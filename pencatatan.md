# API Endpoint
## Pencatatan
- [POST /api/v2/badan-usaha/:id_badan_usaha/pencatatan](#create-new-pencatatan)
- [GET /api/v2/badan-usaha/:id_badan_usaha/pencatatan](#get-all-pencatatan)
- [GET /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan](#get-pencatatan-by-id)
- [PUT /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan](#update-pencatatan)
- [DELETE /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan](#delete-pencatatan)
- [Upload /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/lampiran](#upload-lampiran)
## Perizinan
- [GET /api/v2/badan-usaha/:id_badan_usaha/perizinan](#get-all-perizinan)
- [POST /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan](#create-new-perizinan)
- [GET /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan/:id_perizinan](#get-perizinan-by-id)
- [PUT /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan/:id_perizinan](#update-perizinan)
- [DELETE /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan/:id_perizinan](#delete-perizinan)
- [Upload /api/v2/badan-usaha/:id_badan_usaha/perizinan/lampiran](#upload-lampiran)

### Create new pencatatan
endpoint: `POST /api/v2/badan-usaha/:id_badan_usaha/pencatatan`
payload: 
```json
{
    "jenis_pencatatan": "IUP-IUPK"
}
```

### Get all pencatatan
endpoint: `GET /api/v2/badan-usaha/:id_badan_usaha/pencatatan`


### Get pencatatan by id
endpoint: `GET /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan`

### Update pencatatan
endpoint: `PUT /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan`

### Delete pencatatan
endpoint: `DELETE /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan`

### Upload lampiran pencatatan (Dokumen pendukung)
endpoint: `POST /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/lampiran`

payload: `form-data` dengan key `file` dan value file yang akan diupload
```json
{
    "file": "/path/to/file",
    "nama_lampiran": "nama lampiran",
    "id_jenis_dokumen": 1,
}
```

### Get all perizinan
endpoint: `GET /api/v2/badan-usaha/:id_badan_usaha/perizinan`

### Create new perizinan
endpoint: `POST /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan`
payload: 
```json
{
    "id_wiup": "1",
    "nama_lampiran": "file.pdf",
    "path": "example.com/file.pdf",
    "id_komoditas": "149",
    "id_tahap_kegiatan": "2",
    "id_jenis_perizinan": "1",
    "nomor_izin": "234234",
    "nama_pejabat": "pejabat",
    "jabatan_pejabat": "jabatan_pejabat",
    "kode_kabupaten": "2029",
    "polygon": {
        "type": "Polygon",
        "coordinates": [
            [
                [
                    0,
                    1
                ],
                [
                    0.866,
                    0.5
                ],
                [
                    0.866,
                    -0.5
                ],
                [
                    0,
                    -1
                ],
                [
                    -0.866,
                    -0.5
                ],
                [
                    -0.866,
                    0.5
                ],
                [
                    0,
                    1
                ]
            ]
        ]
    }
}
```

### Get perizinan by id
endpoint: `GET /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan/:id_perizinan`

### Update perizinan
endpoint: `PUT /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan/:id_perizinan`
payload
```json
{
    "id_wiup": "1",
    "nama_lampiran": "file.pdf",
    "path": "example.com/file.pdf",
    "id_komoditas": "149",
    "id_tahap_kegiatan": "2",
    "id_jenis_perizinan": "1",
    "nama_pejabat": "pejabat",
    "jabatan_pejabat": "jabatan_pejabat",
    "kode_kabupaten": "2029",
    "polygon": {
        "type": "Polygon",
        "coordinates": [
            [
                [
                    0,
                    1
                ],
                [
                    0.866,
                    0.5
                ],
                [
                    0.866,
                    -0.5
                ],
                [
                    0,
                    -1
                ],
                [
                    -0.866,
                    -0.5
                ],
                [
                    -0.866,
                    0.5
                ],
                [
                    0,
                    1
                ]
            ]
        ]
    }
}
```

### Delete perizinan
endpoint: `DELETE /api/v2/badan-usaha/:id_badan_usaha/pencatatan/:id_pencatatan/perizinan/:id_perizinan`

### Upload lampiran perizinan (Dokumen SK)
endpoint: `POST /api/v2/badan-usaha/:id_badan_usaha/perizinan/lampiran`
payload `form-data` dengan key `file` dan value file yang akan diupload
```json
{
    "file": "/path/to/file",
    "nama_lampiran": "nama lampiran",
}
```
