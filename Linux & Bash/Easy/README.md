# Easy

---

## 1. "Saint John": what is writing to this log file?

```bash
kill $(lsof /var/log/bad.log | awk 'NR>1 {print $2}')
```

---

## 2. "Saskatoon": counting IPs

```bash
awk '{print $1}' access.log | sort | uniq -c | sort -rn | head -1 | awk '{print $2}' | tee ~/highestip.txt
```

---

## 3. "The Command Line Murders"

```bash
echo "Joe Germuska" > ~/mysolution
```

---

## 7. "Bata": Find in /proc

```bash
grep -r "^secret:" /proc/sys 2>/dev/null | sed 's/.*secret://' > /home/admin/secret.txt
```

---

## 15. "Alexandria": The Vanishing Backups

```bash
sudo rm -f /opt/backup/backup.lock

echo "* * * * * /opt/backup/backup.sh" | sudo crontab -u root -

sudo /opt/backup/backup.sh
```
