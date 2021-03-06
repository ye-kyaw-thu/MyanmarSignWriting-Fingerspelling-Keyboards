# MyanmarSignWriting-Fingerspelling-Keyboards

မြန်မာလိုဖတ်မယ်ဆိုရင် --> [README in Myanmar Language](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/README-Myanmar.md)  

We proposed two fingerspelling keyboard layouts for typing Myanmar fingerspelling characters with [SignWriting](https://en.wikipedia.org/wiki/SignWriting). Fingerspelling is used in sign language to spell out names of people and places for which there is not a sign.  

We learned both Myanmar fingerspelling and SignWriting. The followings are the mapping table of Myanmar characters, fingerspelling and SignWriting.   

### Consonant:  
<p align="center">
 <img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/charmap/consonant.png" alt="consonant" width="500px" height="750px" /> 
</p>

### Vowel:
<p align="center">
<img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/charmap/vowel.png" alt="vowel" width="500x" height="200x" />
</p>

### Independent Vowel:  
<p align="center">
<img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/charmap/independent-vowel1.png" alt="independent-vowel-1" width="500x" height="100x" /><img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/charmap/independent-vowel2.png" alt="independent-vowel-2" width="470x" height="100x" />
</p>

### Symbol:  
<p align="center">
<img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/charmap/symbols.png" alt="symbol" width="500x" height="300x" />
</p>

### Number:  
<p align="center">
<img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/charmap/numbers.png" alt="independent-vowel-2" width="500x" height="180x" />
</p>

## Two Myanmar SignWriting Fingerspelling Keyboards

We proposed two possible keyboard mappings for typing Myanmar fingerspelling with SignWriting symbols and they are phonetic-based and symbol-based keyboard layouts.  

## Phonetic-based MSW Fingerspelling Keyboard:  
<p align="center">
<img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/keyboards/MSW-Fingerspelling-KB-Phonetic-Based.png" alt="phonetic-based-MSW-fingerspelling-keyboard" width="800x" height="300x" />
</p> 

## Symbol-based MSW Fingerspelling Keyboard:  
<p align="center">
<img src="https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/keyboards/MSW-Fingerspelling-KB-Symbol-Based.png" alt="Symbol-based-MSW-Fingerspelling-Keyboard" width="800x" height="300x" />
</p> 

## Demo Videos of Typing Myanmar SignWriting Fingerspelling Text
Demo videos of typing three Myanmar poems with both phonetic-based and symbol-based keyboards are uploaded to GitHub and Youtube. After you downloaded the repository, check the demo-video/ folder.  

Typing a Myanmar poem with phonetic-based Myanmar SignWriting fingerspelling keyboard:

[![Typing a Myanmar poem with phonetic-based Myanmar SignWriting fingerspelling keyboard](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/demo-video/images/image-typing-demo-msw-fs-pho-kb-poem1-btn.png)](https://www.youtube.com/watch?v=NCsfay9HP5M)  

Typing a Myanmar poem with symbol-based Myanmar SignWriting fingerspelling keyboard:

[![Typing a Myanmar poem with symbol-based Myanmar SignWriting fingerspelling keyboard](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/demo-video/images/image-typing-demo-msw-fs-sym-poem2-btn.png)](https://www.youtube.com/watch?v=ih11NG0FTm4&t=13s)  


## Installation  

If you want to add one of the Myanmar SignWriting Fingerspelling keyboards (e.g. phonetic-based keyboard) as a new keyboard layout in your X Windows, take the following steps:  
(I assume you already downloaded xkb keyboard files from this GitHub)

 1. Copy downloaded [msw-fs-phonetic](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/keyboards/msw-fs-phonetic) file to /usr/share/X11/xkb/symbols/ path:
 ```
    sudo cp ~/your-download-path/msw-fs-phonetic /usr/share/X11/xkb/symbols/msw-fs-phonetic
 ```
 2. Change to the path /usr/share/X11/xkb/rules/:
 ```
 cd /usr/share/X11/xkb/rules
 ```
 3. Open evdev.xml file with an editor such as vi, emacs and gedit:
 ```
 sudo gedit evdev.xml
 ```
  put following XML content, save and quit:
 
 ```xml
 <layout> 
      <configItem>
        <name>msw-fs-phonetic</name>
        
        <shortDescription>msw fs phonetic</shortDescription>
        <description>MSW Fingerspelling (Phonetic)</description>
        <languageList>
          <iso639Id>mya</iso639Id>
        </languageList>
      </configItem>
      <variantList/>
    </layout> 
 ```
 
 4. Open evdev.lst file and add following line:
 
 ```
  msw-fs-phonetic             MSW Fingerspelling (Phonetic)
 ```

Adding above line according to the alphabetical order is better for searching (see the following figure):

![adding-in-evdev.lst-file](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/adding-in-evdev.lst-file.png)

5. Open "Text Entry dialogue box" by clicking "US" (If your current keyboard layout is US) and selecting the "Text Entry Settings...".

*Another option: You can also open "Text Entry dialogue box" by clicking the "Settings icon" in the upper-right corner of the screen, select "System Setting..." and then select "Text Entry".*

![text-entry-dialogue-box](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/Text%20Entry_dlBox1.png) 

6. Click the "+" button under the list of installed keyboard layouts and then select "MSW Fingerspelling (Phonetic)" as shown in the following figure:

![choose-an-kkg-input-Source](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/ChooseAnInputSource-msw-fs-pho.png)

7. To test "MSW Fingerspelling (Phonetic)" keyboard layout is working or not, look at the keyboard layout icon, in the upper-right corner of your screen, and then switch your current keyboard layout to "MSW Fingerspelling (Phonetic)" (see following figure).

![selecting-kkg-eg](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/image4readme/select-msw-fs-pho-kb.jpeg)

You can also switch keyboard layout by pressing "Super Key" + "Space Bar".  
Here, "Super Key" is Windows key or Command key.  

Note: Depends on your Ubuntu OS distributions, sometimes you also have to update base.lst, base.xml, xfree86.lst and xfree86.xml. One more information is that you might need to reboot for activating a new keyboard layout.  

## SignWriting Keyboard for Windows OS Users

We developed MSW Fingerspelling (Phonetic) keyboard layout for Windows OS users and released all KeyMan source files on August 25, 2020.  
Check: [https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/tree/master/WindowsOS](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/tree/master/WindowsOS)  

Typing demo video on Windows OS: [https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/tree/master/WindowsOS/demo-video](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/tree/master/WindowsOS/demo-video)  

Draft guide of developing a new SignWriting keyboard layout by using KeyMan Desktop: [https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/WindowsOS/creating-keyboard-draft.pdf](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/WindowsOS/creating-keyboard-draft.pdf)  

## Lincense
MIT License

## Acknowledgement
We would like to thank teachers and students from School for the Deaf, Mandalay and all participants for their kind contributions to our research and user study experiments. This research is partially supported by Ministry of Education, Department of Higher Education, Myanmar.  

## Citing  

Conference Paper:  
Hlaing Myat Nwe, Ye Kyaw Thu, Hnin Wai Wai Hlaing, Swe Zin Moe, Ni Htwe Aung , Hnin Aye Thant , Nanda Win Min, "Two Fingerspelling Keyboard Layouts for Myanmar SignWriting", In Proceedings of ICCA2018, February 22-23, 2018, Yangon, Myanmar, pp. 290-298. [Paper](https://github.com/ye-kyaw-thu/MSL4Emergency/blob/master/publications/msw-fingerspelling-keyboards-ICCA2018.pdf)  

Journal Paper:  
Hlaing Myat Nwe, Ye Kyaw Thu, Hnin Aye Thant, "Myanmar SignWriting Keyboard Mapping Layout for Fingerspelling", Journal of Intelligent Informatics and Smart Technology, April 1st Issue, 2020, pp. 45-52. (submitted December 21, 2019; accepted March 6, 2020; revised April 25, 2020; published online April 30, 2020) [Paper](https://github.com/ye-kyaw-thu/papers/blob/master/JIIST-April-2020/no.6.sw-keyboard-camready.pdf)  

## Presentation at SignWriting Symposium 2018

[Presentation video and slide of MyanmarSignWriting fingerspelling keyboards proposal](http://www.signwriting.org/symposium/presentation0072.html)  

## Reference
Wikipedia of SignWriting: [https://en.wikipedia.org/wiki/SignWriting](https://en.wikipedia.org/wiki/SignWriting)  
Youtube Video of "Valerie Sutton Tells Her Story ...": [https://www.youtube.com/watch?v=xzYW8_Br2MM](https://www.youtube.com/watch?v=xzYW8_Br2MM)  
Sutton SignWriting Unicode standard (version 10.0): [https://unicode.org/charts/PDF/U1D800.pdf](https://unicode.org/charts/PDF/U1D800.pdf)  
kKg Myanmar Keyboard Layout: [https://github.com/ye-kyaw-thu/kKg-Myanmar-Keyboard](https://github.com/ye-kyaw-thu/kKg-Myanmar-Keyboard)  
Keyman Desktop: [https://keyman.com/desktop/](https://keyman.com/desktop/)  

