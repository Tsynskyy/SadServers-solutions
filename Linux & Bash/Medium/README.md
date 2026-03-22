# Medium

---

## 1. "Manhattan": can't write data into database.

```bash
rm /opt/pgdata/deleteme /opt/pgdata/file*.bk
```

---

## 2. "Cape Town": Borked Nginx

```bash
sudo sed -i '1{/^;$/d}' /etc/nginx/sites-enabled/default

sudo sed -i 's/worker_processes auto;/worker_processes auto;\nworker_rlimit_nofile 65535;/' /etc/nginx/nginx.conf

sudo systemctl restart nginx
```

---

## 3. "Oaxaca": Close an Open File

```bash
exec 77>&-
```

---

## 4. "Melbourne": WSGI with Gunicorn

This scenario is only available to Pro or Business users and Im not ready to pay for it :(

---

## 5. "Lisbon": etcd SSL cert troubles

```bash
sudo date -s "2023-01-29"

sudo /usr/sbin/iptables -t nat -F

sudo systemctl restart etcd
```

---

## 6. "Kihei": Surely Not Another Disk Space Scenario

```bash
sudo pvcreate /dev/nvme1n1 /dev/nvme2n1
sudo vgcreate data_vg /dev/nvme1n1 /dev/nvme2n1
sudo lvcreate -l 100%FREE -n data_lv data_vg
sudo mkfs.ext4 /dev/data_vg/data_lv
sudo mount /dev/data_vg/data_lv /home/admin/data
sudo chown admin:admin /home/admin/data
/home/admin/kihei
```

---
