# README

Ansible Playbook untuk installasi LAMP stack + Wordpress di JH VPS Revolusi.

Playbook ini merupakan bagian dari JH Super Template / All in One template.

## OS yang didukung

- CentOS 7
- Debian 9

## Komponen

| Content | Version | License |
| -----    | ---------- | ------ |
| Wordpress | Latest | GPLv2 |
| Apache | 2.4.x | Apache 2 |
| MariaDB | 10.3 | GPLv2 |
| PHP | 7.2 | PHP v3.0.1 |
| Monit | 5.x | AGPL 3.0 |

## Cara menjalankan ansible playbook

1. Clone playbook ini dengan menggunakan perintah `git clone git@gitlab.beon.co.id:ansible-roles/ansible-playbook-wordpress.git`
2. Masuk ke dalam directory playbook dan buat file inventory dan isikan dengan nama server.
3. Setelah siap jalankan perintah berikut untuk menjalankan playbook:
```shell
ansible-playbook -vv -i hosts wordpress.yml
```

## Variable

Berikut adalah list variable yang diperlukan untuk menginstall Wordpress dengan menggunakan playbook ini.

| Variable | Default Value | Keterangan |
| -----    | ---------- | ------ |
| wordpress_db_name | wp_db | nama database yang digunakan oleh Wordpress |
| wordpress_db_user | wp_user | user database untuk koneksi ke database Wordpress |
| wordpress_db_pass | wp_pass | password user database |
| wordpress_blog_url | hostname server | URL yang digunakan untuk akses Wordpress |
| wordpress_blog_admin_name | Admin | Nama user admin |
| wordpress_blog_admin_pass | admin_pass | password admin Wordpress |
| wordpress_blog_admin_email | admin@example.com | alamat email user admin |
| wordpress_php_version | 7.2 | Versi PHP wordpress yang diinginkan |

## Cara kerja/kontribusi di Repository

* Selalu buat branch baru untuk penambahan role, tweak ataupun fix issue
* Pastikan informasi commit jelas. eg: Ubah setting php max execution time