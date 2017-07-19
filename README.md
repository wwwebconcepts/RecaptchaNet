VB.NET RecaptchaNet Class provides simple Google Recaptcha implementation using either the robots or classic Recaptcha interface. 

See Contact.vbhtml for usage example. 

GetControl() function call creates the robots style Google recaptcha control. 

GetControl(theme, language) function call creates the classic style Google recaptcha control. 

RecaptchaNet can be used to secure a form or as gateway page to other content. 
```vbnet
' sample calling code
Dim theCAPTCHA As New ReCAPTCHANet
With theCAPTCHA
  .PrivateKey = "" & ReCAPTCHAPrivateKey & ""
  .PublicKey = "" & ReCAPTCHAPublicKey & ""
  .QueryParameter = "querystring parameter when using redirect. default is Recaptcha="
  .RedirectURL = "redirect to on success"
  .FailURL = "redirect to on fail"
  Construct() ' Returns validation as boolean
End With
' Classic style recaptcha: <div class="recaptcha"><%=theCAPTCHA.getControl("" & ReCAPTCHATheme & "","" & ReCAPTCHALanguage & "")%></div>

' Robots style: <div class="recaptcha"><%=theCAPTCHA.getControl()%></div>
 ```
