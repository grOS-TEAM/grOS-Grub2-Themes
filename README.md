grub2-themes-grombyangOS
========================

![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)
Except where otherwise **noted**, content of grub2-themes-ubuntu-mate by Ivan Pejić aka nadrimajstor is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)
Modify by etcsession <etcsession@gros-team.org>
***


####Manual install
1. Copy .PNGs and theme.txt files to `/boot/grub/themes/grombyangOS`
2. Add to grub's menu.cfg `theme=/boot/grub/themes/grombyangOS/theme.txt` or patch `/lib/plymouth/themes/default.grub`

####Ubuntu-mate specific patch for `/lib/plymouth/themes/default.grub`
```diff
@@ -1,3 +1,10 @@
-if background_color 44,0,30; then
+if background_color 60,59,55; then
   clear
 fi
+
+color_normal=light-gray/black
+
+if [ -e /boot/grub/themes/grombyangOS/theme.txt ]; then
+  insmod png
+  theme=/boot/grub/themes/grombyangOS/theme.txt
+fi
```

**Screenshot** : Grub2 Themes
![grOS Grub2 Screenshot](https://raw.githubusercontent.com/grOS-TEAM/grOS-Grub2-Themes/master/screenshot.jpg)
