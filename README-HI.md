# Market OS Android APK project

यह project तुम्हारी upgraded professional `index.html` वाली Market OS demo app को Android WebView app में पैक करने के लिए है।

## इसमें क्या है?
- Customer और Shopkeeper demo signup/login
- Logout
- अलग dashboard और navigation
- Products, cart और demo booking requests
- Shopkeeper demo product management
- Local demo AI assistant
- Terms & Disclaimer page
- Android WebView wrapper
- GitHub Actions workflow जो debug APK बनाता है

## फोन से APK बनाने का तरीका
1. ZIP को फोन में डाउनलोड करके extract करो।
2. GitHub पर नया repository बनाओ, उदाहरण: `market-os-android`.
3. ZIP के अंदर की सारी files और folders repository के root में upload करो। `.github/workflows/build-apk.yml` भी मौजूद होना चाहिए।
4. `Actions` tab खोलो। अगर workflow permission मांगे तो enable करो।
5. `Build Market OS APK` workflow चुनकर `Run workflow` दबाओ। `main` branch पर push करने से भी build शुरू होगा।
6. Build सफल होने पर workflow run खोलो, नीचे `Artifacts` में `Market-OS-debug-APK` डाउनलोड करो।
7. ZIP artifact को extract करो और `app-debug.apk` को Android phone पर install करो। Android अगर पूछे तो केवल तभी “Install unknown apps” की अनुमति दो जब तुम इस APK और उसके source पर भरोसा करते हो।

## जरूरी सीमाएँ
- यह **debug APK** है, Play Store release APK नहीं।
- Login/password अभी सिर्फ demo/local browser storage में है; production-secure authentication नहीं है।
- Real payments, Supabase database, live AI API, merchant notifications या server-side booking अभी connected नहीं हैं।
- Demo password के लिए असली password इस्तेमाल मत करना।
- Production में release करने से पहले secure backend, privacy policy, payment gateway, app signing और legal review जरूरी हैं।
