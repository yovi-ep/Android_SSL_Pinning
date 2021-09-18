# Android_SSL_Pinning
Documentation Only

Step - step generate BKS File
1. Need certicates file from server/backend side
2. We need to download bouncy castle jar to create BKS file. The bouncy castle is a crypto API. You can download the latest release from this repo.
3. Generate File BKS using scrip:
keytool -importcert -v -trustcacerts -file "/user/mert/testcertificate.cer" -alias mytestalias -keystore "/user/mert/desktop/certificate.bks" -provider org.bouncycastle.jce.provider.BouncyCastleProvider -providerpath "/user/mert/bcprov-jdk15on-159.jar" -storetype BKS -storepass mypassword
4. Put the BKS file to your app proeckt (res/raw/)
5. Add SSL pinning to network tools, there is using okhttp, you can download from this repo (xxx.file)
