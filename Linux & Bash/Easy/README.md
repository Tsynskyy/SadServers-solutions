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

## 4. "Resumable Server": Linux Upskill Challenge

No challenge. Start and stop the server to complete

---

## 5. "Lhasa": Easy Math

```bash
awk '{sum += $2} END {printf "%.2f\n", sum/NR}' scores.txt > ~/solution
```

---

## 6. "Apia": Needle in a Haystack

This scenario is only available to Pro or Business users and Im not ready to pay for it :(

---

## 7. "Bata": Find in /proc

```bash
grep -r "^secret:" /proc/sys 2>/dev/null | sed 's/.*secret://' > /home/admin/secret.txt
```

---

## 8. Linux Server Review - Guided Learning

No challenge. Start and stop the server to complete

---

## 9. "Tokamachi": Troubleshooting a Named Pipe

```bash
/bin/bash -c 'while true; do echo "this is a test message being sent to the pipe" > /home/admin/namedpipe; sleep 5; done' &
```

---

## 14. "Cairo": Time for a Timer

```bash
sudo iptables -D OUTPUT 1

sudo systemctl enable --now health.timer
```

---

## 15. "Alexandria": The Vanishing Backups

```bash
sudo rm -f /opt/backup/backup.lock

echo "* * * * * /opt/backup/backup.sh" | sudo crontab -u root -

sudo /opt/backup/backup.sh
```
