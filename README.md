# සිංහල Keyboard එක සකස් කිරීම

Settings යෙදුම විවෘත කරගන්න
![image](https://user-images.githubusercontent.com/2894127/163845431-5bc83a9e-ef9e-45da-9b7c-b77d3f8ec82b.png)


![image](https://user-images.githubusercontent.com/2894127/163844372-ae80b3e6-ebec-45e8-9289-df7d2d3e8051.png)

මෙහි Input sources කොටසෙ දැනටම සිංහල නැති නම්, පහල ඇති + සලකුණ තෝරා එතනින් Sinhala (Wijesekara(m17n) යන්න තෝරන්න. 

![image](https://user-images.githubusercontent.com/2894127/163844643-2eb9f4e3-a22a-439c-afc2-b3cc138c08b3.png)

සිංහල සහ ඉංග්‍රිසි keyboard දෙක අතර මාරු වීමට Shift සහ Super Key(WinKey) සමඟ Space එකවර ඔබන්න. 

# කැමති සිංහල අකුරක් ස්ථාපනය කිරීම
සාමාන්යෙන් Ubuntu එකත් එක්කක Default Sinhala font එක විදියට එන්නේනේ  LKLug කියන සිංහල Font එක. මේ අකුරට අකමැති අයට තමං කැමති Font එකක් ස්ථාපනය කරගන්නේ මෙහෙමයි.

මුලින්මම ඔබ කැමති Font එක Download කරලා install කරන්න. පුද්ගලිකව මම වඩාත් කැමතියි Abhaya Libre කියන font එකට. ටිකක් ලොකු පැහැදිලිව වෙන් වෙන්වව පේන අකුරු වලට කැමති නම් Noto Font එක ගැලපේවි.

- [Abhaya Libre](https://fonts.google.com/specimen/Abhaya+Libre)
- [Noto San Sinhala](https://fonts.google.com/noto/specimen/Noto+Sans+Sinhala)
- [Noto Serif Sinhala](https://fonts.google.com/noto/specimen/Noto+Serif+Sinhala)

දැනට පරිගණකයේ සිංහල අකුරු තියෙනන Fonts List එක බලාගන්නන ඕන නම් පහත command එක ගහල බලන්න.
`fc-list :lang=si`

`lklug.ttf file` එකත් ඒ අතර තියේවි. ඒක තියෙන path එක බලාගෙන ඒ font එක remove කරන්නන පුළුවන්. නැතිනම් වෙනත් folder එකකට backup කරගන්න.

`/etc/fonts/conf.d/65-sinhala.conf` කියලා අලුතින් file එකක් හදලා ඒකට  පහත තියෙන content එක කොපි කරන්න.
```
?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
  <its:rules xmlns:its="http://www.w3.org/2005/11/its" version="1.0">
    <its:translateRule translate="no" selector="/fontconfig/*[not(self::description)]"/>
  </its:rules>

        <alias>
                <family>serif</family>
                <prefer>
                        <family>Abhaya Libre</family>
                </prefer>
        </alias>
        <alias>
                <family>sans-serif</family>
                <prefer>
                        <family>Abhaya Libre</family>
                </prefer>
        </alias>
</fontconfig>
```
දැන් හරි. එක් වරක් පරිගණකය restart කරන්න. සාමාන්යෙන් ඔබට LKLug font එක remove නොකරත් මේක කරන්නන පුළුවන් වෙන්නන ඕන. ඒත් Chrome වගේ browser මොකක් හරි හේතුවක් නිසා LKLUG font එකින් අකුරු පෙන්වන ගැටළුවක් මට පුද්ගලිකව තිබ්බා. ඒක නිසා LKLUG font එක ඉවත් කිරීම පහසුවක් වුනා. 


