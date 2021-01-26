# Display Kecepatan Mengetik

### Display WPM untuk web 10fastfingers.com
![Display](https://cdn.discordapp.com/attachments/638665637111267332/803579666467782707/unknown.png)

## Typing Speed Indicator

-Silahkan kunjungi web [ini](https://10fastfingers.com/)
-Tekan ``F12`` di keyboard, kalo gada keyboard bisa klik kanan mouse lalu ``inspect``
-Klik Tab ``cosole``
-Paste code di bawah kedalam ``console``

```js
$(function () 
{
    $(document).keydown(function (k) 
    {
        realWPM = Math.round((error_keystrokes / 5) / ((60.01 - countdown) / 60));

    if(realWPM < 0 || realWPM > 400)
        {
            realWPM = 0;
        }

        $('#preview').html("<font size='+3'><b>WPM:</b> " + 
        realWPM + "<br><b>Key Strokes:</b> " + 
        error_keystrokes + "<br><b>Words:</b> " + 
        error_correct + "</<font size='+3'>");

        $('#words').before("<div id='preview'></div>");
    })
})
```
-Done