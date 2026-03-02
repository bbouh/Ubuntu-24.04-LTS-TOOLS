# دليل شامل: أدوات مدير النظام - Ubuntu 24.04 LTS

> **الإصدار:** Ubuntu 24.04 LTS (Noble Numbat)  
> **التاريخ:** مارس 2026  
> **الغرض:** قائمة كاملة بجميع أدوات إدارة النظام من الأصغر إلى الأكبر

---

## 📋 جدول المحتويات

1. [أدوات النظام الأساسية](#أدوات-النظام-الأساسية)
2. [أدوات إدارة العمليات](#أدوات-إدارة-العمليات)
3. [أدوات إدارة الشبكات](#أدوات-إدارة-الشبكات)
4. [أدوات إدارة التخزين والأقراص](#أدوات-إدارة-التخزين-والأقراص)
5. [أدوات المراقبة والأداء](#أدوات-المراقبة-والأداء)
6. [أدوات الأمان](#أدوات-الأمان)
7. [أدوات إدارة الحزم](#أدوات-إدارة-الحزم)
8. [أدوات النسخ الاحتياطي والاستعادة](#أدوات-النسخ-الاحتياطي-والاستعادة)
9. [أدوات إدارة المستخدمين والصلاحيات](#أدوات-إدارة-المستخدمين-والصلاحيات)
10. [أدوات السجلات والتشخيص](#أدوات-السجلات-والتشخيص)
11. [أدوات الأتمتة والبرمجة](#أدوات-الأتمتة-والبرمجة)
12. [أدوات التحكم بالخدمات](#أدوات-التحكم-بالخدمات)
13. [أدوات الأداء المتقدمة](#أدوات-الأداء-المتقدمة)
14. [أدوات واجهات الرسومية](#أدوات-واجهات-الرسومية)
15. [طرق التثبيت لبيئة Offline](#طرق-التثبيت-لبيئة-offline)

---

## 1. أدوات النظام الأساسية

### 1.1 أوامر التنقل والملفات الأساسية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `ls` | coreutils | عرض محتويات المجلدات | ⭐⭐⭐⭐⭐ |
| `cd` | bash (مدمج) | التنقل بين المجلدات | ⭐⭐⭐⭐⭐ |
| `pwd` | coreutils | عرض المسار الحالي | ⭐⭐⭐⭐⭐ |
| `mkdir` | coreutils | إنشاء مجلدات | ⭐⭐⭐⭐⭐ |
| `rmdir` | coreutils | حذف مجلدات فارغة | ⭐⭐⭐⭐ |
| `rm` | coreutils | حذف ملفات ومجلدات | ⭐⭐⭐⭐⭐ |
| `cp` | coreutils | نسخ ملفات ومجلدات | ⭐⭐⭐⭐⭐ |
| `mv` | coreutils | نقل/إعادة تسمية | ⭐⭐⭐⭐⭐ |
| `touch` | coreutils | إنشاء ملفات فارغة | ⭐⭐⭐⭐ |
| `cat` | coreutils | عرض محتوى الملفات | ⭐⭐⭐⭐⭐ |
| `less` | less | عرض ملفات كبيرة | ⭐⭐⭐⭐⭐ |
| `more` | util-linux | عرض ملفات (أساسي) | ⭐⭐⭐ |
| `head` | coreutils | عرض أول سطور | ⭐⭐⭐⭐ |
| `tail` | coreutils | عرض آخر سطور | ⭐⭐⭐⭐⭐ |
| `file` | file | معرفة نوع الملف | ⭐⭐⭐⭐ |
| `stat` | coreutils | معلومات تفصيلية عن ملف | ⭐⭐⭐⭐ |

### 1.2 أدوات البحث والتصفية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `find` | findutils | البحث عن ملفات | ⭐⭐⭐⭐⭐ |
| `locate` | mlocate | بحث سريع بقاعدة بيانات | ⭐⭐⭐⭐ |
| `updatedb` | mlocate | تحديث قاعدة بيانات locate | ⭐⭐⭐⭐ |
| `grep` | grep | البحث داخل الملفات | ⭐⭐⭐⭐⭐ |
| `egrep` | grep | grep متقدم | ⭐⭐⭐⭐ |
| `fgrep` | grep | بحث سريع ثابت | ⭐⭐⭐ |
| `ripgrep (rg)` | ripgrep | بحث فائق السرعة | ⭐⭐⭐⭐⭐ |
| `ag (silver-searcher)` | silversearcher-ag | بحث سريع للكود | ⭐⭐⭐⭐ |
| `fzf` | fzf | بحث تفاعلي ضبابي | ⭐⭐⭐⭐⭐ |
| `which` | debianutils | موقع الأوامر | ⭐⭐⭐⭐⭐ |
| `whereis` | util-linux | البحث عن ملفات البرامج | ⭐⭐⭐⭐ |
| `apropos` | man-db | البحث في صفحات المساعدة | ⭐⭐⭐ |

### 1.3 أدوات معالجة النصوص

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `sed` | sed | معالج نصوص stream | ⭐⭐⭐⭐⭐ |
| `awk` | gawk | معالجة بيانات نصية | ⭐⭐⭐⭐⭐ |
| `cut` | coreutils | استخراج أعمدة | ⭐⭐⭐⭐ |
| `paste` | coreutils | دمج أسطر | ⭐⭐⭐ |
| `sort` | coreutils | ترتيب النصوص | ⭐⭐⭐⭐⭐ |
| `uniq` | coreutils | إزالة التكرار | ⭐⭐⭐⭐ |
| `tr` | coreutils | تحويل/حذف أحرف | ⭐⭐⭐⭐ |
| `wc` | coreutils | عد الكلمات والأسطر | ⭐⭐⭐⭐⭐ |
| `diff` | diffutils | مقارنة ملفات | ⭐⭐⭐⭐⭐ |
| `patch` | patch | تطبيق الفروقات | ⭐⭐⭐⭐ |
| `comm` | coreutils | مقارنة ملفات مرتبة | ⭐⭐⭐ |
| `tee` | coreutils | قراءة وكتابة معاً | ⭐⭐⭐⭐ |
| `xargs` | findutils | بناء وتنفيذ أوامر | ⭐⭐⭐⭐⭐ |
| `column` | util-linux | تنسيق نص بأعمدة | ⭐⭐⭐ |

### 1.4 المحررات النصية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `nano` | nano | محرر سهل للمبتدئين | ⭐⭐⭐⭐⭐ |
| `vim` | vim | محرر قوي متقدم | ⭐⭐⭐⭐⭐ |
| `vi` | vim-tiny | محرر أساسي | ⭐⭐⭐⭐⭐ |
| `emacs` | emacs | محرر شامل متقدم | ⭐⭐⭐⭐ |
| `joe` | joe | محرر بسيط وسريع | ⭐⭐⭐ |
| `micro` | micro | محرر حديث سهل | ⭐⭐⭐⭐ |
| `neovim` | neovim | vim محسن | ⭐⭐⭐⭐ |

---

## 2. أدوات إدارة العمليات

### 2.1 مراقبة العمليات الأساسية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `ps` | procps | عرض العمليات | ⭐⭐⭐⭐⭐ |
| `top` | procps | مراقبة فورية للعمليات | ⭐⭐⭐⭐⭐ |
| `htop` | htop | top متقدم وملون | ⭐⭐⭐⭐⭐ |
| `atop` | atop | مراقبة شاملة للنظام | ⭐⭐⭐⭐ |
| `btop` | btop | مراقب حديث جذاب | ⭐⭐⭐⭐ |
| `glances` | glances | لوحة مراقبة شاملة | ⭐⭐⭐⭐⭐ |
| `nmon` | nmon | أداء مفصل | ⭐⭐⭐⭐ |

### 2.2 التحكم بالعمليات

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `kill` | procps | إنهاء عملية | ⭐⭐⭐⭐⭐ |
| `killall` | psmisc | إنهاء عمليات بالاسم | ⭐⭐⭐⭐⭐ |
| `pkill` | procps | إنهاء بنمط | ⭐⭐⭐⭐⭐ |
| `pgrep` | procps | البحث عن عمليات | ⭐⭐⭐⭐⭐ |
| `nice` | coreutils | تشغيل بأولوية | ⭐⭐⭐⭐ |
| `renice` | util-linux | تغيير الأولوية | ⭐⭐⭐⭐ |
| `bg` | bash (مدمج) | تشغيل في الخلفية | ⭐⭐⭐⭐ |
| `fg` | bash (مدمج) | إحضار للمقدمة | ⭐⭐⭐⭐ |
| `jobs` | bash (مدمج) | عرض الوظائف | ⭐⭐⭐⭐ |
| `nohup` | coreutils | تشغيل مستمر | ⭐⭐⭐⭐⭐ |
| `screen` | screen | جلسات طرفية متعددة | ⭐⭐⭐⭐⭐ |
| `tmux` | tmux | multiplexer متقدم | ⭐⭐⭐⭐⭐ |
| `disown` | bash (مدمج) | فصل عملية | ⭐⭐⭐ |

### 2.3 أدوات جدولة المهام

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `cron` | cron | جدولة دورية | ⭐⭐⭐⭐⭐ |
| `crontab` | cron | إدارة مهام cron | ⭐⭐⭐⭐⭐ |
| `at` | at | جدولة مرة واحدة | ⭐⭐⭐⭐ |
| `batch` | at | تنفيذ عند انخفاض الحمل | ⭐⭐⭐ |
| `anacron` | anacron | مهام غير معتمدة على وقت | ⭐⭐⭐⭐ |
| `systemd-timer` | systemd | مؤقتات systemd | ⭐⭐⭐⭐⭐ |

---

## 3. أدوات إدارة الشبكات

### 3.1 أدوات الشبكات الأساسية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `ip` | iproute2 | إدارة شاملة للشبكة | ⭐⭐⭐⭐⭐ |
| `ifconfig` | net-tools | إعدادات الشبكة (قديم) | ⭐⭐⭐⭐ |
| `ping` | iputils-ping | اختبار الاتصال | ⭐⭐⭐⭐⭐ |
| `ping6` | iputils-ping | ping لـ IPv6 | ⭐⭐⭐⭐ |
| `traceroute` | traceroute | تتبع المسار | ⭐⭐⭐⭐⭐ |
| `tracepath` | iputils-tracepath | تتبع بسيط | ⭐⭐⭐⭐ |
| `mtr` | mtr | traceroute مستمر | ⭐⭐⭐⭐⭐ |
| `netstat` | net-tools | إحصائيات الشبكة | ⭐⭐⭐⭐⭐ |
| `ss` | iproute2 | فحص sockets (بديل netstat) | ⭐⭐⭐⭐⭐ |
| `route` | net-tools | إدارة الطرق | ⭐⭐⭐⭐ |
| `arp` | net-tools | جدول ARP | ⭐⭐⭐⭐ |
| `arping` | arping | إرسال ARP requests | ⭐⭐⭐ |
| `hostname` | hostname | اسم الجهاز | ⭐⭐⭐⭐⭐ |
| `host` | bind9-host | استعلامات DNS | ⭐⭐⭐⭐⭐ |
| `dig` | bind9-dnsutils | استعلام DNS متقدم | ⭐⭐⭐⭐⭐ |
| `nslookup` | bind9-dnsutils | بحث DNS (قديم) | ⭐⭐⭐⭐ |

### 3.2 أدوات التشخيص والمراقبة

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `tcpdump` | tcpdump | التقاط حزم الشبكة | ⭐⭐⭐⭐⭐ |
| `wireshark` | wireshark | تحليل حزم رسومي | ⭐⭐⭐⭐⭐ |
| `tshark` | tshark | wireshark طرفي | ⭐⭐⭐⭐⭐ |
| `nmap` | nmap | فحص الشبكة والمنافذ | ⭐⭐⭐⭐⭐ |
| `netcat (nc)` | netcat-openbsd | أداة شبكة متعددة | ⭐⭐⭐⭐⭐ |
| `socat` | socat | تحويل بيانات متقدم | ⭐⭐⭐⭐ |
| `telnet` | telnet | اتصال بعيد (غير آمن) | ⭐⭐⭐ |
| `wget` | wget | تحميل من الإنترنت | ⭐⭐⭐⭐⭐ |
| `curl` | curl | نقل بيانات متقدم | ⭐⭐⭐⭐⭐ |
| `iftop` | iftop | مراقبة استخدام الشبكة | ⭐⭐⭐⭐⭐ |
| `iptraf-ng` | iptraf-ng | مراقبة IP تفاعلية | ⭐⭐⭐⭐ |
| `nethogs` | nethogs | استهلاك الشبكة للعمليات | ⭐⭐⭐⭐⭐ |
| `bmon` | bmon | مراقبة bandwidth | ⭐⭐⭐⭐ |
| `vnstat` | vnstat | إحصائيات شبكة طويلة المدى | ⭐⭐⭐⭐ |
| `speedtest-cli` | speedtest-cli | اختبار سرعة الإنترنت | ⭐⭐⭐⭐ |
| `ethtool` | ethtool | إدارة ethernet | ⭐⭐⭐⭐⭐ |
| `iwconfig` | wireless-tools | إعداد WiFi | ⭐⭐⭐⭐ |
| `iw` | iw | إدارة WiFi حديثة | ⭐⭐⭐⭐⭐ |

### 3.3 أدوات Firewall والأمان

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `iptables` | iptables | جدار حماية قديم | ⭐⭐⭐⭐⭐ |
| `nftables` | nftables | جدار حماية حديث | ⭐⭐⭐⭐⭐ |
| `ufw` | ufw | جدار حماية بسيط | ⭐⭐⭐⭐⭐ |
| `firewalld` | firewalld | إدارة جدار حماية | ⭐⭐⭐⭐ |
| `fail2ban` | fail2ban | منع الهجمات | ⭐⭐⭐⭐⭐ |

### 3.4 أدوات SSH و Remote

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `ssh` | openssh-client | اتصال آمن بعيد | ⭐⭐⭐⭐⭐ |
| `sshd` | openssh-server | خادم SSH | ⭐⭐⭐⭐⭐ |
| `ssh-keygen` | openssh-client | إنشاء مفاتيح SSH | ⭐⭐⭐⭐⭐ |
| `ssh-copy-id` | openssh-client | نسخ مفاتيح | ⭐⭐⭐⭐⭐ |
| `scp` | openssh-client | نسخ آمن | ⭐⭐⭐⭐⭐ |
| `sftp` | openssh-client | نقل ملفات آمن | ⭐⭐⭐⭐⭐ |
| `rsync` | rsync | مزامنة فعّالة | ⭐⭐⭐⭐⭐ |
| `sshfs` | sshfs | mount عبر SSH | ⭐⭐⭐⭐ |

---

## 4. أدوات إدارة التخزين والأقراص

### 4.1 أدوات الأقراص الأساسية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `df` | coreutils | مساحة الأقراص | ⭐⭐⭐⭐⭐ |
| `du` | coreutils | استهلاك المساحة | ⭐⭐⭐⭐⭐ |
| `mount` | util-linux | تركيب أنظمة ملفات | ⭐⭐⭐⭐⭐ |
| `umount` | util-linux | فك التركيب | ⭐⭐⭐⭐⭐ |
| `lsblk` | util-linux | عرض الأقراص | ⭐⭐⭐⭐⭐ |
| `blkid` | util-linux | معرفات الأقراص | ⭐⭐⭐⭐⭐ |
| `fdisk` | util-linux | تقسيم الأقراص | ⭐⭐⭐⭐⭐ |
| `parted` | parted | تقسيم متقدم | ⭐⭐⭐⭐⭐ |
| `gparted` | gparted | تقسيم رسومي | ⭐⭐⭐⭐⭐ |
| `cfdisk` | util-linux | تقسيم تفاعلي | ⭐⭐⭐⭐ |
| `sfdisk` | util-linux | تقسيم نصي | ⭐⭐⭐ |
| `gdisk` | gdisk | تقسيم GPT | ⭐⭐⭐⭐⭐ |

### 4.2 أدوات أنظمة الملفات

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `mkfs` | util-linux | إنشاء نظام ملفات | ⭐⭐⭐⭐⭐ |
| `mkfs.ext4` | e2fsprogs | إنشاء ext4 | ⭐⭐⭐⭐⭐ |
| `mkfs.xfs` | xfsprogs | إنشاء XFS | ⭐⭐⭐⭐⭐ |
| `mkfs.btrfs` | btrfs-progs | إنشاء Btrfs | ⭐⭐⭐⭐ |
| `fsck` | util-linux | فحص نظام الملفات | ⭐⭐⭐⭐⭐ |
| `e2fsck` | e2fsprogs | فحص ext2/3/4 | ⭐⭐⭐⭐⭐ |
| `xfs_repair` | xfsprogs | إصلاح XFS | ⭐⭐⭐⭐⭐ |
| `tune2fs` | e2fsprogs | ضبط ext2/3/4 | ⭐⭐⭐⭐ |
| `resize2fs` | e2fsprogs | تغيير حجم ext | ⭐⭐⭐⭐ |
| `xfs_growfs` | xfsprogs | تكبير XFS | ⭐⭐⭐⭐ |

### 4.3 LVM (Logical Volume Manager)

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `pvcreate` | lvm2 | إنشاء physical volume | ⭐⭐⭐⭐⭐ |
| `pvdisplay` | lvm2 | عرض PV | ⭐⭐⭐⭐⭐ |
| `pvs` | lvm2 | قائمة PVs مختصرة | ⭐⭐⭐⭐⭐ |
| `vgcreate` | lvm2 | إنشاء volume group | ⭐⭐⭐⭐⭐ |
| `vgdisplay` | lvm2 | عرض VG | ⭐⭐⭐⭐⭐ |
| `vgs` | lvm2 | قائمة VGs | ⭐⭐⭐⭐⭐ |
| `vgextend` | lvm2 | توسيع VG | ⭐⭐⭐⭐ |
| `lvcreate` | lvm2 | إنشاء logical volume | ⭐⭐⭐⭐⭐ |
| `lvdisplay` | lvm2 | عرض LV | ⭐⭐⭐⭐⭐ |
| `lvs` | lvm2 | قائمة LVs | ⭐⭐⭐⭐⭐ |
| `lvextend` | lvm2 | توسيع LV | ⭐⭐⭐⭐⭐ |
| `lvresize` | lvm2 | تغيير حجم LV | ⭐⭐⭐⭐⭐ |

### 4.4 أدوات RAID

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `mdadm` | mdadm | إدارة RAID | ⭐⭐⭐⭐⭐ |
| `raid-check` | mdadm | فحص RAID | ⭐⭐⭐⭐ |

### 4.5 أدوات التشفير

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `cryptsetup` | cryptsetup | تشفير LUKS | ⭐⭐⭐⭐⭐ |
| `dm-crypt` | cryptsetup | تشفير device mapper | ⭐⭐⭐⭐⭐ |

### 4.6 أدوات متقدمة للتخزين

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `ncdu` | ncdu | تحليل مساحة تفاعلي | ⭐⭐⭐⭐⭐ |
| `duf` | duf | df حديث | ⭐⭐⭐⭐ |
| `smartctl` | smartmontools | فحص صحة الأقراص | ⭐⭐⭐⭐⭐ |
| `hdparm` | hdparm | معلومات الأقراص | ⭐⭐⭐⭐ |
| `sdparm` | sdparm | معلومات SCSI | ⭐⭐⭐ |
| `ddrescue` | gddrescue | استعادة بيانات | ⭐⭐⭐⭐⭐ |
| `dd` | coreutils | نسخ قطاعات | ⭐⭐⭐⭐⭐ |

---

## 5. أدوات المراقبة والأداء

### 5.1 مراقبة الموارد

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `vmstat` | procps | إحصائيات ذاكرة افتراضية | ⭐⭐⭐⭐⭐ |
| `iostat` | sysstat | إحصائيات I/O | ⭐⭐⭐⭐⭐ |
| `mpstat` | sysstat | إحصائيات معالج | ⭐⭐⭐⭐⭐ |
| `sar` | sysstat | تقارير نشاط النظام | ⭐⭐⭐⭐⭐ |
| `free` | procps | معلومات الذاكرة | ⭐⭐⭐⭐⭐ |
| `uptime` | procps | وقت التشغيل والحمل | ⭐⭐⭐⭐⭐ |
| `w` | procps | من متصل والأنشطة | ⭐⭐⭐⭐ |
| `who` | coreutils | المستخدمون المتصلون | ⭐⭐⭐⭐ |
| `last` | util-linux | سجل تسجيل الدخول | ⭐⭐⭐⭐⭐ |
| `lastlog` | login | آخر تسجيل دخول | ⭐⭐⭐⭐ |

### 5.2 أدوات Profiling والتحليل

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `strace` | strace | تتبع system calls | ⭐⭐⭐⭐⭐ |
| `ltrace` | ltrace | تتبع library calls | ⭐⭐⭐⭐ |
| `lsof` | lsof | ملفات مفتوحة | ⭐⭐⭐⭐⭐ |
| `fuser` | psmisc | من يستخدم الملف | ⭐⭐⭐⭐ |
| `perf` | linux-tools | أداء kernel | ⭐⭐⭐⭐⭐ |
| `sysdig` | sysdig | تحليل نظام شامل | ⭐⭐⭐⭐⭐ |
| `bpftrace` | bpftrace | تتبع eBPF | ⭐⭐⭐⭐ |

### 5.3 أدوات درجة الحرارة والطاقة

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `sensors` | lm-sensors | درجات الحرارة | ⭐⭐⭐⭐⭐ |
| `acpi` | acpi | معلومات البطارية | ⭐⭐⭐⭐ |
| `powertop` | powertop | استهلاك الطاقة | ⭐⭐⭐⭐ |
| `cpupower` | linux-cpupower | إدارة المعالج | ⭐⭐⭐⭐ |

---

## 6. أدوات الأمان

### 6.1 أدوات الأمان الأساسية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `sudo` | sudo | تنفيذ بصلاحيات عليا | ⭐⭐⭐⭐⭐ |
| `su` | util-linux | تبديل مستخدم | ⭐⭐⭐⭐⭐ |
| `visudo` | sudo | تحرير sudoers آمن | ⭐⭐⭐⭐⭐ |

### 6.2 SELinux و AppArmor

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `apparmor_status` | apparmor-utils | حالة AppArmor | ⭐⭐⭐⭐⭐ |
| `aa-enforce` | apparmor-utils | فرض profile | ⭐⭐⭐⭐ |
| `aa-complain` | apparmor-utils | وضع تسامح | ⭐⭐⭐⭐ |
| `aa-disable` | apparmor-utils | تعطيل profile | ⭐⭐⭐⭐ |

### 6.3 فحص الثغرات والأمان

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `lynis` | lynis | تدقيق أمني | ⭐⭐⭐⭐⭐ |
| `rkhunter` | rkhunter | كشف rootkit | ⭐⭐⭐⭐⭐ |
| `chkrootkit` | chkrootkit | فحص rootkit | ⭐⭐⭐⭐ |
| `aide` | aide | كشف التسلل | ⭐⭐⭐⭐ |
| `clamav` | clamav | مضاد فيروسات | ⭐⭐⭐⭐ |
| `openvas` | openvas | فحص ثغرات | ⭐⭐⭐⭐⭐ |
| `nikto` | nikto | فحص خوادم الويب | ⭐⭐⭐⭐ |
| `tripwire` | tripwire | سلامة الملفات | ⭐⭐⭐⭐ |

### 6.4 أدوات التشفير والشهادات

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `openssl` | openssl | تشفير وشهادات | ⭐⭐⭐⭐⭐ |
| `gpg` | gnupg | تشفير GPG | ⭐⭐⭐⭐⭐ |
| `certbot` | certbot | شهادات Let's Encrypt | ⭐⭐⭐⭐⭐ |

---

## 7. أدوات إدارة الحزم

### 7.1 APT (Advanced Package Tool)

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `apt` | apt | إدارة حزم حديثة | ⭐⭐⭐⭐⭐ |
| `apt-get` | apt | إدارة حزم تقليدية | ⭐⭐⭐⭐⭐ |
| `apt-cache` | apt | البحث في الحزم | ⭐⭐⭐⭐⭐ |
| `apt-file` | apt-file | البحث عن ملفات | ⭐⭐⭐⭐ |
| `dpkg` | dpkg | إدارة حزم .deb | ⭐⭐⭐⭐⭐ |
| `dpkg-query` | dpkg | استعلام الحزم | ⭐⭐⭐⭐⭐ |
| `dpkg-reconfigure` | debconf | إعادة إعداد حزمة | ⭐⭐⭐⭐ |
| `apt-mark` | apt | وضع علامات حزم | ⭐⭐⭐⭐ |
| `apt-key` | apt | إدارة مفاتيح | ⭐⭐⭐⭐ |
| `add-apt-repository` | software-properties-common | إضافة مستودعات | ⭐⭐⭐⭐⭐ |

### 7.2 Snap و Flatpak

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `snap` | snapd | حزم snap | ⭐⭐⭐⭐⭐ |
| `flatpak` | flatpak | حزم flatpak | ⭐⭐⭐⭐ |

### 7.3 أدوات البناء

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `build-essential` | build-essential | أدوات تطوير أساسية | ⭐⭐⭐⭐⭐ |
| `make` | make | بناء برامج | ⭐⭐⭐⭐⭐ |
| `cmake` | cmake | نظام بناء متقدم | ⭐⭐⭐⭐⭐ |
| `gcc` | gcc | مترجم C | ⭐⭐⭐⭐⭐ |
| `g++` | g++ | مترجم C++ | ⭐⭐⭐⭐⭐ |
| `checkinstall` | checkinstall | تحويل لحزمة | ⭐⭐⭐⭐ |

---

## 8. أدوات النسخ الاحتياطي والاستعادة

### 8.1 أدوات النسخ الاحتياطي

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `rsync` | rsync | مزامنة ونسخ | ⭐⭐⭐⭐⭐ |
| `tar` | tar | أرشفة ملفات | ⭐⭐⭐⭐⭐ |
| `gzip` | gzip | ضغط gzip | ⭐⭐⭐⭐⭐ |
| `bzip2` | bzip2 | ضغط bzip2 | ⭐⭐⭐⭐ |
| `xz` | xz-utils | ضغط xz | ⭐⭐⭐⭐⭐ |
| `zip` | zip | أرشيف zip | ⭐⭐⭐⭐⭐ |
| `unzip` | unzip | فك zip | ⭐⭐⭐⭐⭐ |
| `7z` | p7zip-full | ضغط 7z | ⭐⭐⭐⭐ |
| `rar` | rar | أرشيف rar | ⭐⭐⭐ |
| `unrar` | unrar | فك rar | ⭐⭐⭐⭐ |
| `borgbackup` | borgbackup | نسخ احتياطي مشفر | ⭐⭐⭐⭐⭐ |
| `restic` | restic | نسخ احتياطي سريع | ⭐⭐⭐⭐⭐ |
| `duplicity` | duplicity | نسخ مشفر تزايدي | ⭐⭐⭐⭐ |
| `bacula` | bacula | نظام نسخ شبكي | ⭐⭐⭐⭐ |
| `amanda` | amanda | نسخ شبكي متقدم | ⭐⭐⭐ |

### 8.2 أدوات Snapshot

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `timeshift` | timeshift | نسخ نظام | ⭐⭐⭐⭐⭐ |
| `snapper` | snapper | إدارة snapshots | ⭐⭐⭐⭐ |

---

## 9. أدوات إدارة المستخدمين والصلاحيات

### 9.1 إدارة المستخدمين

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `useradd` | passwd | إضافة مستخدم | ⭐⭐⭐⭐⭐ |
| `usermod` | passwd | تعديل مستخدم | ⭐⭐⭐⭐⭐ |
| `userdel` | passwd | حذف مستخدم | ⭐⭐⭐⭐⭐ |
| `adduser` | adduser | إضافة تفاعلية | ⭐⭐⭐⭐⭐ |
| `deluser` | adduser | حذف تفاعلي | ⭐⭐⭐⭐ |
| `passwd` | passwd | تغيير كلمة مرور | ⭐⭐⭐⭐⭐ |
| `chage` | passwd | إدارة انتهاء كلمة مرور | ⭐⭐⭐⭐ |
| `id` | coreutils | معرف المستخدم | ⭐⭐⭐⭐⭐ |
| `whoami` | coreutils | المستخدم الحالي | ⭐⭐⭐⭐⭐ |

### 9.2 إدارة المجموعات

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `groupadd` | passwd | إضافة مجموعة | ⭐⭐⭐⭐⭐ |
| `groupmod` | passwd | تعديل مجموعة | ⭐⭐⭐⭐ |
| `groupdel` | passwd | حذف مجموعة | ⭐⭐⭐⭐ |
| `groups` | coreutils | مجموعات المستخدم | ⭐⭐⭐⭐⭐ |
| `gpasswd` | passwd | إدارة مجموعات | ⭐⭐⭐⭐ |
| `newgrp` | login | تبديل مجموعة | ⭐⭐⭐ |

### 9.3 الصلاحيات وملكية الملفات

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `chmod` | coreutils | تغيير صلاحيات | ⭐⭐⭐⭐⭐ |
| `chown` | coreutils | تغيير المالك | ⭐⭐⭐⭐⭐ |
| `chgrp` | coreutils | تغيير المجموعة | ⭐⭐⭐⭐ |
| `umask` | bash (مدمج) | صلاحيات افتراضية | ⭐⭐⭐⭐ |
| `setfacl` | acl | ACL متقدم | ⭐⭐⭐⭐ |
| `getfacl` | acl | عرض ACL | ⭐⭐⭐⭐ |

---

## 10. أدوات السجلات والتشخيص

### 10.1 إدارة السجلات

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `journalctl` | systemd | سجلات systemd | ⭐⭐⭐⭐⭐ |
| `logger` | bsdutils | كتابة لسجل النظام | ⭐⭐⭐⭐ |
| `rsyslog` | rsyslog | نظام سجلات | ⭐⭐⭐⭐⭐ |
| `logrotate` | logrotate | تدوير السجلات | ⭐⭐⭐⭐⭐ |
| `dmesg` | util-linux | رسائل kernel | ⭐⭐⭐⭐⭐ |
| `multitail` | multitail | متابعة عدة سجلات | ⭐⭐⭐⭐ |

### 10.2 أدوات التشخيص

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `uname` | coreutils | معلومات النظام | ⭐⭐⭐⭐⭐ |
| `lscpu` | util-linux | معلومات المعالج | ⭐⭐⭐⭐⭐ |
| `lshw` | lshw | عتاد شامل | ⭐⭐⭐⭐⭐ |
| `lspci` | pciutils | أجهزة PCI | ⭐⭐⭐⭐⭐ |
| `lsusb` | usbutils | أجهزة USB | ⭐⭐⭐⭐⭐ |
| `dmidecode` | dmidecode | معلومات BIOS | ⭐⭐⭐⭐⭐ |
| `hwinfo` | hwinfo | معلومات عتاد مفصلة | ⭐⭐⭐⭐ |
| `inxi` | inxi | معلومات نظام سريعة | ⭐⭐⭐⭐ |
| `neofetch` | neofetch | معلومات جمالية | ⭐⭐⭐ |
| `screenfetch` | screenfetch | معلومات نظام | ⭐⭐⭐ |

---

## 11. أدوات الأتمتة والبرمجة

### 11.1 Shell Scripting

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `bash` | bash | shell أساسي | ⭐⭐⭐⭐⭐ |
| `sh` | dash | POSIX shell | ⭐⭐⭐⭐⭐ |
| `zsh` | zsh | shell متقدم | ⭐⭐⭐⭐ |
| `fish` | fish | shell حديث | ⭐⭐⭐ |
| `shellcheck` | shellcheck | فحص scripts | ⭐⭐⭐⭐⭐ |

### 11.2 لغات البرمجة

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `python3` | python3 | Python 3 | ⭐⭐⭐⭐⭐ |
| `pip3` | python3-pip | إدارة حزم Python | ⭐⭐⭐⭐⭐ |
| `perl` | perl | لغة Perl | ⭐⭐⭐⭐ |
| `ruby` | ruby | لغة Ruby | ⭐⭐⭐ |
| `node` | nodejs | JavaScript runtime | ⭐⭐⭐⭐ |
| `npm` | npm | إدارة حزم Node | ⭐⭐⭐⭐ |

### 11.3 أدوات التحكم بالإصدارات

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `git` | git | نظام تحكم بالإصدارات | ⭐⭐⭐⭐⭐ |
| `gitk` | gitk | واجهة رسومية لـ git | ⭐⭐⭐ |
| `tig` | tig | واجهة طرفية لـ git | ⭐⭐⭐⭐ |

---

## 12. أدوات التحكم بالخدمات

### 12.1 Systemd

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `systemctl` | systemd | التحكم بالخدمات | ⭐⭐⭐⭐⭐ |
| `systemd-analyze` | systemd | تحليل الإقلاع | ⭐⭐⭐⭐⭐ |
| `hostnamectl` | systemd | إدارة اسم الجهاز | ⭐⭐⭐⭐ |
| `timedatectl` | systemd | إدارة الوقت والتاريخ | ⭐⭐⭐⭐⭐ |
| `localectl` | systemd | إعدادات اللغة | ⭐⭐⭐⭐ |
| `loginctl` | systemd | إدارة الجلسات | ⭐⭐⭐⭐ |

### 12.2 SysV (قديم)

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `service` | sysvinit-utils | إدارة خدمات | ⭐⭐⭐ |
| `update-rc.d` | init-system-helpers | إدارة runlevels | ⭐⭐⭐ |

---

## 13. أدوات الأداء المتقدمة

### 13.1 Benchmarking

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `sysbench` | sysbench | قياس أداء شامل | ⭐⭐⭐⭐⭐ |
| `stress` | stress | اختبار إجهاد | ⭐⭐⭐⭐ |
| `stress-ng` | stress-ng | اختبار إجهاد متقدم | ⭐⭐⭐⭐⭐ |
| `fio` | fio | قياس أداء I/O | ⭐⭐⭐⭐⭐ |
| `iperf3` | iperf3 | قياس أداء الشبكة | ⭐⭐⭐⭐⭐ |
| `bonnie++` | bonnie++ | قياس أداء أقراص | ⭐⭐⭐⭐ |

---

## 14. أدوات واجهات الرسومية

### 14.1 أدوات إدارة رسومية

| الأداة | الحزمة | الاستخدام | الأهمية |
|-------|--------|----------|---------|
| `gnome-system-monitor` | gnome-system-monitor | مراقب نظام GNOME | ⭐⭐⭐⭐ |
| `cockpit` | cockpit | لوحة إدارة ويب | ⭐⭐⭐⭐⭐ |
| `webmin` | webmin | إدارة عبر الويب | ⭐⭐⭐⭐ |

---

## 15. طرق التثبيت لبيئة Offline

### 15.1 إنشاء مستودع محلي كامل

#### الطريقة الأولى: apt-mirror

**على جهاز متصل بالإنترنت:**

```bash
# تثبيت apt-mirror
sudo apt install apt-mirror

# إعداد المستودعات المطلوبة
sudo nano /etc/apt/mirror.list

# محتوى الملف:
############# config ##################
set base_path    /var/spool/apt-mirror
set mirror_path  $base_path/mirror
set skel_path    $base_path/skel
set var_path     $base_path/var
set defaultarch  amd64
set postmirror_script $var_path/postmirror.sh
set run_postmirror 0
set nthreads     20
set _tilde 0

############# end config ##############

# Ubuntu 24.04 Main
deb http://archive.ubuntu.com/ubuntu noble main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu noble-updates main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu noble-backports main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu noble-security main restricted universe multiverse

# بدء المزامنة (يحتاج ~200GB مساحة)
sudo apt-mirror

# ضغط المستودع
cd /var/spool/apt-mirror
sudo tar -czf ubuntu-24.04-mirror.tar.gz mirror/

# نقل للجهاز Offline
```

**على الجهاز Offline:**

```bash
# فك الضغط
sudo mkdir -p /var/spool/apt-mirror
sudo tar -xzf ubuntu-24.04-mirror.tar.gz -C /var/spool/apt-mirror

# إعداد خادم محلي (اختياري)
sudo apt install apache2
sudo ln -s /var/spool/apt-mirror/mirror/archive.ubuntu.com/ubuntu /var/www/html/ubuntu

# أو استخدام مباشرة
sudo nano /etc/apt/sources.list

# استبدال المحتوى بـ:
deb [trusted=yes] file:///var/spool/apt-mirror/mirror/archive.ubuntu.com/ubuntu noble main restricted universe multiverse
deb [trusted=yes] file:///var/spool/apt-mirror/mirror/archive.ubuntu.com/ubuntu noble-updates main restricted universe multiverse

# تحديث
sudo apt update
```

### 15.2 تحميل حزم محددة

#### الطريقة الثانية: apt-offline

```bash
# على جهاز Offline
sudo apt install apt-offline
apt-offline set offline-requirements.sig --update

# نقل ملف .sig لجهاز متصل

# على جهاز متصل
sudo apt install apt-offline
sudo apt-offline get offline-requirements.sig --bundle offline-data.zip

# نقل offline-data.zip للجهاز Offline

# على جهاز Offline
sudo apt-offline install offline-data.zip
sudo apt update
```

#### الطريقة الثالثة: apt-get download

```bash
# على جهاز متصل
mkdir ~/offline-packages
cd ~/offline-packages

# تحميل حزمة واعتمادياتها
apt-get download $(apt-cache depends --recurse --no-recommends --no-suggests --no-conflicts --no-breaks --no-replaces --no-enhances htop | grep "^\w" | sort -u)

# أو استخدام apt-get مع --download-only
sudo apt-get install --download-only -y htop

# الحزم في: /var/cache/apt/archives/

# نسخ جميع الحزم
cp /var/cache/apt/archives/*.deb ~/offline-packages/

# نقل للجهاز Offline
# على الجهاز Offline
sudo dpkg -i *.deb
```

### 15.3 إنشاء قرص التثبيت الموسع

```bash
# تحميل ISO أساسي
wget https://releases.ubuntu.com/24.04/ubuntu-24.04-server-amd64.iso

# mount الصورة
sudo mkdir /mnt/iso
sudo mount -o loop ubuntu-24.04-server-amd64.iso /mnt/iso

# نسخ المحتوى
sudo mkdir ~/custom-iso
sudo cp -rT /mnt/iso ~/custom-iso

# إضافة حزم إضافية
sudo mkdir ~/custom-iso/extra-packages
sudo cp ~/offline-packages/*.deb ~/custom-iso/extra-packages/

# إعادة بناء ISO
sudo apt install xorriso
sudo xorriso -as mkisofs \
  -r -V "Ubuntu 24.04 Custom" \
  -o ubuntu-24.04-custom.iso \
  -J -l -b isolinux/isolinux.bin \
  -c isolinux/boot.cat \
  -no-emul-boot -boot-load-size 4 \
  -boot-info-table ~/custom-iso
```

### 15.4 استخدام USB كمستودع محلي

```bash
# تحضير USB
sudo mkfs.ext4 /dev/sdX1
sudo mkdir /mnt/usb
sudo mount /dev/sdX1 /mnt/usb

# نسخ المستودع
sudo rsync -av /var/spool/apt-mirror/mirror/ /mnt/usb/ubuntu-repo/

# على جهاز Offline
sudo mount /dev/sdX1 /mnt/usb
echo "deb [trusted=yes] file:///mnt/usb/ubuntu-repo/archive.ubuntu.com/ubuntu noble main restricted universe multiverse" | sudo tee /etc/apt/sources.list.d/usb-repo.list
sudo apt update
```

---

## 📊 إحصائيات الملف

- **إجمالي الأدوات المذكورة:** 400+ أداة
- **الفئات الرئيسية:** 15 فئة
- **الحزم الأساسية:** 200+ حزمة
- **مساحة المستودع الكامل:** ~200GB
- **التوزيع:** Ubuntu 24.04 LTS

---

## 🔄 تحديثات مستقبلية

يُنصح بتحديث هذه القائمة كل 6 أشهر لمواكبة:
- إصدارات الحزم الجديدة
- الأدوات الحديثة
- التغييرات في Ubuntu 24.04

---

## 📝 ملاحظات إضافية

1. **الأولويات:** الأدوات ذات ⭐⭐⭐⭐⭐ ضرورية لكل مدير نظام
2. **التوافق:** جميع الأدوات متوافقة مع Ubuntu 24.04 LTS
3. **الأمان:** تحديث الأدوات الأمنية بانتظام حتى في بيئة Offline
4. **التدريب:** يُنصح بالتدرب على الأدوات في بيئة اختبار أولاً

---

**تم الإعداد:** مارس 2026  
**المؤلف:** دليل شامل لمديري أنظمة Ubuntu
