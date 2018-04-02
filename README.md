# MyanmarSignWriting-Fingerspelling-Keyboards
We proposed two fingerspelling keyboard layouts for typing Myanmar fingerspelling characters with [SignWriting](https://en.wikipedia.org/wiki/SignWriting). Fingerspelling is used in sign language to spell out names of people and places for which there is not a sign.

ReadMe file is still preparing ...

မြန်မာလိုဖတ်မယ်ဆိုရင် --> [README in Myanmar Language](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/README-Myanmar.md)  

## Demo Videos of Typing Myanmar SignWriting Fingerspelling Text
Typing demo videos of three Myanmar poems with both phonetic-based and symbol-based keyboards are uploaded to GitHub and Youtube.  
After you downloaded, check the demo-video/ folder.  

Typing a Myanmar poem with phonetic-based Myanmar SignWriting fingerspelling keyboard:

[![Typing a Myanmar poem with phonetic-based Myanmar SignWriting fingerspelling keyboard](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/demo-video/images/image-typing-demo-msw-fs-pho-kb-poem1-btn.png)](https://www.youtube.com/watch?v=NCsfay9HP5M)  

Typing a Myanmar poem with symbol-based Myanmar SignWriting fingerspelling keyboard:

[![Typing a Myanmar poem with symbol-based Myanmar SignWriting fingerspelling keyboard](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/demo-video/images/image-typing-demo-msw-fs-sym-poem2-btn.png)](https://www.youtube.com/watch?v=ih11NG0FTm4&t=13s)  


## Installation  
To writedown some installation steps ...  

### Installation Method  
If you want to add one of the Myanmar SignWriting Fingerspelling keyboards as a new keyboard layout in your X Windows:  
(I assume you already downloaded xkb keyboard files from this GitHub)

 1. Copy downloaded [msw-fs-phonetic](https://github.com/ye-kyaw-thu/MyanmarSignWriting-Fingerspelling-Keyboards/blob/master/keyboards/msw-fs-phonetic) symbols file to /usr/share/X11/xkb/symbols/ path:
 ```
    sudo cp ~/your-download-path/msw-fs-phonetic /usr/share/X11/xkb/symbols/msw-fs-phonetic
 ```
 2. Change to /usr/share/X11/xkb/rules/:
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

7. To test "MSW Fingerspelling (Phonetic)" keyboard layout is working or not, look at the keyboard layout icon, in the upper-right corner of your screen, and then switch your current keyboard layout to "kKg (Myanmar)" (see following figure).

![selecting-kkg-eg](https://github.com/ye-kyaw-thu/kKg-Myanmar-Keyboard/blob/master/xkb-intro/selecting-kkg-eg.jpg)

You can also switch keyboard layout by pressing "Super Key" + "Space Bar". Here, "Super Key" is Windows key or Command key.

Note: Depends on your Ubuntu OS distributions, sometimes you also have to update base.lst, base.xml, xfree86.lst, xfree86.xml as I mentioned in step 3 and 4. One more information is that I have to reboot for activating a new keyboard layout on Ubuntu OS 14.04 LTS computer.  

## Lincense
MIT License

## Acknowledgement
We would like to thank teachers and students from School for the Deaf, Mandalay and all participants for their kind contributions to our research and user study experiments. This research is partially supported by Ministry of Education, Department of Higher Education, Myanmar.  

## Citing  
Hlaing Myat Nwe, Ye Kyaw Thu, Hnin Wai Wai Hlaing, Swe Zin Moe, Ni Htwe Aung , Hnin Aye Thant , Nanda Win Min, "Two Fingerspelling Keyboard Layouts for Myanmar SignWriting", In Proceedings of ICCA2018, February 22-23, 2018, Yangon, Myanmar, pp. 290-298. [Paper](https://github.com/ye-kyaw-thu/MSL4Emergency/blob/master/publications/msw-fingerspelling-keyboards-ICCA2018.pdf)  

## Reference

[Sutton SignWriting Unicode standard (version 10.0)](https://unicode.org/charts/PDF/U1D800.pdf)  
[kKg Myanmar Keyboard Layout](https://github.com/ye-kyaw-thu/kKg-Myanmar-Keyboard)  
