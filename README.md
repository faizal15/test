# README

Ansible Playbook untuk installasi Gitlab di JH VPS X.

Playbook ini merupakan bagian dari JH Super Template / All in One template.

## OS yang didukung

- CentOS 7 Minimal (VM/VZ)
- Ubuntu 18 Minimal (VM/VZ)

## Requirements

- Ram Minimal 4GB (untuk 500 user)
- Ram 8GB (1000 user)

## Komponen

| Content | Version | License |
| -----    | ---------- | ------ |
| Gitlab | 13.11.2 | MIT License |
| Postfix | 3.3.0 | IBM Public License |

## Cara menjalankan ansible playbook

1. Clone playbook ini dengan menggunakan perintah `git clone git@gitlab.beon.co.id:internship-projects/x-cube-installer/ansible-playbook-gitlab.git`
2. Masuk ke dalam directory playbook dan buat file inventory dan isikan dengan nama server.
3. Setelah siap jalankan perintah berikut untuk menjalankan playbook:
```shell
ansible-playbook -vvv -i hosts gitlab.yml
```

## Variable

Berikut adalah list variable yang diperlukan untuk menginstall Gitlab menggunakan playbook ini.

| Variable | Default Value | Keterangan |
| -----    | ---------- | ------ |
| gitlab_domain | gitlab.test | Domain yang akan digunakan oleh Gitlab |
| gitlab_external_url | http://{{ gitlab_domain }} | URL eksternal yang akan digunakan oleh Gitlab |


## Cara kerja/kontribusi di Repository

* Selalu buat branch baru untuk penambahan role, tweak ataupun fix issue
* Pastikan informasi commit jelas. eg: Ubah setting php max execution time


