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

## 7. "Paris": Where is my webserver?

```bash
echo "FDZPmh5AX3oiJt" > ~/mysolution
```

---

## 8. "Marrakech": Word Histogram

```bash
grep -oE '[[:alpha:]]+' frankestein.txt | tr '[:upper:]' '[:lower:]' | sort | uniq -c | sort -nr | head -n 2 | tail -n 1 | awk '{print $2}' | tr '[:lower:]' '[:upper:]' > /home/admin/mysolution
```

---

## 9. "Manado": How much do you press?

This scenario is only available to Pro or Business users and Im not ready to pay for it :(

---

## 10. "Moyogalpa": Security Snag. The Trials of Mary and John

```bash
sudo chown -vR webapp:webapp /home/webapp/pki
sudo chmod -v 0600 /home/webapp/pki/server.crt /home/webapp/pki/server.pem

sudo chown -Rv webapp:webapp /home/webapp/static-files
sudo chmod -Rv 0640 /home/webapp/static-files/*

sudo cp -v /home/webapp/pki/CA.crt /usr/local/share/ca-certificates/CA.crt
sudo chmod 0644 /usr/local/share/ca-certificates/CA.crt
sudo update-ca-certificates

echo '127.0.10.1 webapp' | sudo tee -a /etc/hosts

sudo sed -i '/^}/i\  /home\/webapp\/static-files\/ r,\n  /home\/webapp\/static-files\/* r,' /etc/apparmor.d/usr.local.bin.webapp
sudo apparmor_parser -r /etc/apparmor.d/usr.local.bin.webapp
```

---

## 11. "Bekasi": Supervisor is still around

This scenario is only available to Pro or Business users and Im not ready to pay for it :(

---

## 12. "Tukaani": XZ LZMA Library Compromised

This scenario is only available to Pro or Business users and Im not ready to pay for it :(

---

## 13. "Hanoi": Find the Multitasking Users

This scenario is only available to Pro or Business users and Im not ready to pay for it :(

---

## 14. "Batumi": Troubleshoot "A" cannot connect to "B"

This scenario is only available to Pro or Business users and Im not ready to pay for it :(

---

## 15. "Budapest": User Creation

```bash
while IFS=';' read -r login password; do
  ENCRYPTED_PW=$(openssl passwd -1 "$password")
  sudo useradd -m -p "$ENCRYPTED_PW" -s /usr/sbin/nologin "$login"
done < user_list.txt
```

---

## 16. "Tokelau": Delete from history

```bash
sed -i '/foo/d' ~/.bash_history
sed -i '/bash_history/d' ~/.bash_history
```

---

## 17. "Bizerte": The Slow Application

```bash
sudo sed -i 's/REDIS_HOST=127.0.0.2/REDIS_HOST=127.0.0.1/' /etc/systemd/system/slow-app.service
sudo systemctl daemon-reload
sudo systemctl restart slow-app
```

---
