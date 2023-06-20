# How to watch live Now TV and Sky Go italian channels for free and without any VPN

If you're a fan of movies and/or TV series, you definetly will be interested in knowing that you can watch the whole Now TV / Sky Go catalog for free and without any country restriction!

NOW and Sky Go are 2 online streaming platforms that offers a large assortment of content, such as movies, TV series, documentaries, cartoons and much much more.

# How to watch the Sky streams directly using an online player:
In order to access the online catalog without paying anything, you just have to follow those steps:
 
1. Go to your interested section ([Entertainment](#entertainment), [Movies](#cinema), [Sport](#sport) and [Kids](#kids))
2. Click on the live channel you're interested
3. Enjoy!
 
# Requirements
- The only requirement is compatibility with PlayReady HW (we let the DRM decrypt and play the content providing directly the decryption key) and the use of Microsoft Edge.

# If you have DRM_NO_KEY_SYSTEM in Bitmovin and you're using Edge on Windows 10+...
It probably mean that your system doesn't support PlayReady Hardware DRM. You can check that by going to about://gpu in Microsoft Edge and check for those two things:
- "PlayReady Hardware DRM disabled" must be set to false
- "Direct Composition" must be set to true

If one of those 2 settings are not matching, you can give a last chance by upgrading your GPU drivers and check again if they magically changed.
Otherwise, you need to decrypt the streams by yourself using [decryption keys](#decryption-keys), but some coding knowledge are required as playing MSS segments is tricky.
I might post in future something regarding that but it's not planned.
 
# Disclaimer
All the informations provided in this repository are for informational purposes only
The author is not responsible for any loss or damage arising from the use of those informations
The author also wishes to emphasize that this text is not intended to promote piracy or any other illegal activity.

**Even if BSkyB has already been informed of the content decryption keys leakage, instead of changing them (and fix the problem) they still prefer to take down the repository**

**So since this may go down from a moment to another, share this as much as you can!**

We invite users to buy a regular NOW subscription and respect the copyright laws.

# How it works
Encode in Base64 the content decryption key for the desired channel in the license URL [PlayReady Test](https://testweb.playready.microsoft.com/).
After having build the license URL, we have to pass the parameters to [Bitmovin](https://bitmovin.com/demos/stream-test) in order to play the content.
The prebuild URLs are present at the bottom of the page if you are lazy and you want to watch the streams directly

# Decryption keys

**Use them if you are a developer and want to build your own plugin (Kodi developers are welcome) or play them your own way**

| Channel name | Manifest url | kid | key |
| --- | --- | --- | --- |
| Sky TG24 HD | http://hss-live-hd-nowtv.skycdn.it/21519/FHD/tg24.isml/Manifest | c787163ec63d4190b601c61208538d7c | a873db9e680f11ec6b35587c2bc07944 |
| Sky Uno HD | http://hss-live-hd-nowtv.skycdn.it/23477/FHD/skyuno.isml/Manifest | 6cf24f79a08b43c6af7176a79304ab50 | 278124797d6552f87ca9dfe610402cc4 |
| Sky Atlantic HD | http://hss-live-hd-nowtv.skycdn.it/22226/FHD/skyatlantic.isml/Manifest | c9a9974d06104c50a6ee6fe837dc5a22 | a0e53f7c1bc06bfce644cd280c9f6199 |
| Sky Serie HD | http://hss-live-hd-nowtv.skycdn.it/23684/FHD/skyserie.isml/Manifest | d30dbaa77b934294be3b712325b9fc5d | f1e2bc1c6a76b42845d17b611fa6fed4 |
| Comedy Central SD | http://hss-live-nowtv.skycdn.it/22404/comedycentral.isml/Manifest | 4491c7b96ac44626ba5029e9ba15c5c3 | a19ad7c5a26d1584491e7fd32e2bc83f |
| History HD | http://hss-live-hd-nowtv.skycdn.it/21513/FHD/history.isml/Manifest | e62190c77dbb434c8923224fd549e310 | 0fd6becadc373fd67e0c814acd693d98 |
| Sky Investigation HD | http://hss-live-hd-nowtv.skycdn.it/23686/FHD/skyinvestigation.isml/Manifest | 1ae035983a4e4a498da597f29cd4e620 | a91e4808a363aaa81f31a437d695bd3a |
| Crime Investigation HD | http://hss-live-hd-nowtv.skycdn.it/21249/FHD/crimeinvestigation.isml/Manifest | 70e574464f494a53842311bef2c98e39 | 6977c1c51ce3e7f28bac418854df2981 |
| MTV HD | http://hss-live-hd-nowtv.skycdn.it/21763/FHD/mtvnext.isml/Manifest | fc2ab8311d724ce590300fa86fea6e23 | bfb0f9dd7ba2b005834a5dbb629e6a6e |
| Sky Arte HD | http://hss-live-hd-nowtv.skycdn.it/22074/FHD/skyarte.isml/Manifest | b14b309ced384cf5b1d42cc969a73b07 | 8cc8756857f46064a4db0ca4e680084f |
| Sky Documentaries HD | http://hss-live-hd-nowtv.skycdn.it/23697/FHD/skydocumentaries.isml/Manifest | 82f2f171a91c4b5490837ee884de5a52 | 13dc868aee5cc1b70ef4ea2dfc873686 |
| Sky Nature HD | http://hss-live-hd-nowtv.skycdn.it/22695/FHD/skynature.isml/Manifest | 5c9e47a904ea499a997ae749a02c8dd0 | ec6127b88b1eb49f779835bb4fa63f48 |
| Sky Cinema Uno HD | http://hss-live-hd-nowtv.skycdn.it/22202/FHD/cinemauno.isml/Manifest | 5a9b722665254b2d9369c502bb60669c | 7430935f40a12feb7c20fe7a4bd89789 |
| Sky Cinema Comedy HD | http://hss-live-hd-nowtv.skycdn.it/22030/FHD/cinemacomedy.isml/Manifest | f6a83c5b1f674bf8829bb726dc69a96c | 6b65b6fbd3056c8af0addfa19059e2e4 |
| Sky Cinema Action HD | http://hss-live-hd-nowtv.skycdn.it/22206/FHD/cinemaaction.isml/Manifest | 9761541d110047349833509045fc8452 | 0dc1cb98f5eaf91f10f14834d0805330 |
| Sky Cinema Due HD | http://hss-live-hd-nowtv.skycdn.it/22564/FHD/cinemadue.isml/Manifest | d2420fd4b85b40fd93c40d4225dca933 | db2aab2c6c5626918c89aa9f6efed0d7 |
| Sky Cinema Collection HD | http://hss-live-hd-nowtv.skycdn.it/22204/FHD/cinemacollection.isml/Manifest | 68d47db34865471fb663397b04d06254 | c994d851d6bffdb2e691b2effe10e816 |
| Sky Cinema Family HD | http://hss-live-hd-nowtv.skycdn.it/22255/FHD/cinemafamily.isml/Manifest | 30df32a7429e4335a79a939315804c2a | bdb351073e4c46bd981248b08950b59e |
| Sky Cinema Suspense HD | http://hss-live-hd-nowtv.skycdn.it/22047/FHD/cinemasuspense.isml/Manifest | 813153ea2a254b8491dd32eac7c2c0f5 | 5e450e813cae7e1cd6e431271cdbeb7b |
| Sky Cinema Romance HD | http://hss-live-hd-nowtv.skycdn.it/22231/FHD/cinemaromance.isml/Manifest | a8ad76aba2864ce2aa53b05f35ba667f | dab361e629d274b0a02119407fce8afb |
| Sky Cinema Drama HD | http://hss-live-hd-nowtv.skycdn.it/22769/FHD/cinemadrama.isml/Manifest | f9f40f27b8f043ca82c776ae00134a0d | ca664f27d77d8ce123f1d09448d68311 |
| Sky Sport 24 HD | http://hss-live-hd-nowtv.skycdn.it/23035/FHD/skysport24.isml/Manifest | 939b0eb3aff746d6904ed5b192e5c10c | 03cef3e95f11f0292cddf7f0d42bf216 |
| Sky Sport Uno HD | http://hss-live-hd-nowtv.skycdn.it/23023/FHD/skysportuno.isml/Manifest | b9fd6af212944c879239bcec7e17238c | c8d9ed7de4c662b5740cb78b3674a621 |
| Sky Sport F1 HD | http://hss-live-hd-nowtv.skycdn.it/23478/FHD/skysportf1.isml/Manifest | 5261866de7d64eb5aec8ba61c89b0de7 | 397ee8c6a48d9334452ffd67d6e5ab50 |
| Sky Sport MotoGP HD | http://hss-live-hd-nowtv.skycdn.it/23483/FHD/skysportmotogp.isml/Manifest | fd2a64c2c31942678a5724843ee5eb3b | bed2c851b5724d23c93e78ee47089452 |
| Sky Sport Calcio HD | http://hss-live-hd-nowtv.skycdn.it/23209/FHD/skysportseriea.isml/Manifest | 2d9f30b7da0c466ba77651a6c62d1371 | 9ab38e3def7a4ed6f836d176079678d5 |
| Sky Sport Football HD | http://hss-live-hd-nowtv.skycdn.it/21248/FHD/skysportfootball.isml/Manifest | 39e4bc0d3bb54dd1867b4a1a4fa55983 | 3a40b31e15d83cd037a634a8683a4456 |
| Sky Sport Tennis HD | http://hss-live-hd-nowtv.skycdn.it/22559/FHD/skysporttennis.isml/Manifest | e1c15df2107d4386b745a109ee1062d9 | a0e5d02ab249aacc29f7f2c2c1275b85 |
| Sky Sport Arena HD | http://hss-live-hd-nowtv.skycdn.it/23024/FHD/skysportarena.isml/Manifest | d7c95c3be3d740c2a24bc0fa65c74aac | 344c2f34ba62cf4ca7b3a8ed0f8e281c |
| Sky Sport NBA HD | http://hss-live-hd-nowtv.skycdn.it/21764/FHD/skysportnba.isml/Manifest | 6f41da5304c448a6a8b5870922c91613 | d6ba5566006cfd990d34bbb8021d52f8 |
| Sky Sport Golf HD | http://hss-live-hd-nowtv.skycdn.it/23768/FHD/skysportcollection.isml/Manifest | 9e640436bbd240fc8af116ec4209c17c | 988bd191fb45540993b45d62af25c046 |
| Eurosport 1 HD | http://hss-live-hd-nowtv.skycdn.it/213073/FHD/eurosport.isml/Manifest | 7511454fe63a4ed9ae62fdd99dead940 | 7c9e73e5418b5da4c367e6a02a458bf0 |
| Eurosport 2 HD | http://hss-live-hd-nowtv.skycdn.it/21150/FHD/eurosport2.isml/Manifest | 623f8ba057b448faadca887dea10aa6f | 595abbb2908cb495e596c9d151828851 |
| Sky Sport 251 HD | http://hss-live-hd-nowtv.skycdn.it/21917/FHD/skysport251.isml/Manifest | 7e9a9a8ae2dd493087508bc026ab1a28 | fb305293b759b4261223d9570eeb1186 |
| Sky Sport 252 HD | http://hss-live-hd-nowtv.skycdn.it/22951/FHD/skysport252.isml/Manifest | 5cc88c7c08a0416099f701178efad7aa | c2adda0ae88ff95aa4bfa1d62ba75948 |
| Sky Sport 253 HD | http://hss-live-hd-nowtv.skycdn.it/23233/FHD/skysport253.isml/Manifest | 2909cac649464acf850afa9248739edd | 436136b6045ae986fb578aa265bc26d9 |
| Sky Sport 254 HD | http://hss-live-hd-nowtv.skycdn.it/21234/FHD/skysport254.isml/Manifest | 3f0dea6c8bb840a4b8022b6b84209a69 | a133ada8fac0a3c2ee83099aa6371a98 |
| Sky Sport 255 HD | http://hss-live-hd-nowtv.skycdn.it/22910/FHD/skysport255.isml/Manifest | b82a2d3bafd54cb38e73c2ec8696de38 | ef9be15185deeb1a4c17f7dcd39f5345 |
| Sky Sport 256 HD | http://hss-live-hd-nowtv.skycdn.it/23912/FHD/skysport256.isml/Manifest | cd03cb78966349578465335a6e3656b8 | 966cee44e722c91b4a17f26b2afa34b5 |
| Sky Sport 257 HD | http://hss-live-hd-nowtv.skycdn.it/21775/FHD/skysport257.isml/Manifest | 4a3dd36daf764697b1ae71b858a5851c | dab619195e968fa905059f688bac1e52 |
| Sky Sport 258 HD | http://hss-live-hd-nowtv.skycdn.it/22772/FHD/skysport258.isml/Manifest | 6da7e81650b1469d82744c51872058ab | 45955ac1d110262823808ef8f7ddf1d9 |
| Sky Sport 259 SD | http://hss-live-nowtv.skycdn.it/23613/skysport259.isml/Manifest | 0a897acee54e46bfa9e4ac63a6df875b | 5c2bb493f49d9c50102787e493aecdf5 |
| Sky Sport 260 SD | http://hss-live-nowtv.skycdn.it/23615/skysport260.isml/Manifest | 38828cdedd86415789e31e9d5e7293e1 | 6e3d7d817f1ad4621d56cfbf94a3d835 |
| Sky Sport 261 SD | http://hss-live-nowtv.skycdn.it/21617/skysport261.isml/Manifest | 9782111f89774d9b8d4392830757c5be | 81c96ba6071e833df7448048f1eea842 |
| Cartoon Network HD | http://hss-live-hd-nowtv.skycdn.it/21258/FHD/cartoonnetwork.isml/Manifest | e48066a7d0c944ebb5bb92f9b36a240b | f84ed4f28b667baa4ab5262177deaf4b |
| Nickelodeon SD | http://hss-live-nowtv.skycdn.it/21320/nickelodeon.isml/Manifest | 9a7455ab56fa427da7ac038676b6d555 | cb8be5a2f8e2d6b0740b746768d5e587 |
| DeAKids SD | http://hss-live-nowtv.skycdn.it/22460/deakids.isml/Manifest | 43efc829c4b743e6935b515738af5fe0 | e805cd88a7f6da32e97b82807ebbc047 |
| Nick Jr. SD | http://hss-live-nowtv.skycdn.it/22424/nickj.isml/Manifest | 983e1cc915ca447bbdac7c40afc631b1 | dbee39dce07d7c1cbe24ffa52b74e4a1 |
| Boomerang SD | http://hss-live-nowtv.skycdn.it/21367/boomerang.isml/Manifest | 544256ec7f464e78a46afcf911c6a5cf | b298d8005636e2350a5104cf89c9d31a |
 
# Entertainment
- [Sky TG24 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21519%2FFHD%2Ftg24.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AqHPbnmgPEexrNVh8K8B5RA%3D%3D%2Ckid%3Aheader%29)
- [Sky Uno HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23477%2FFHD%2Fskyuno.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AJ4EkeX1lUvh8qd%2FmEEAsxA%3D%3D%2Ckid%3Aheader%29)
- [Sky Atlantic HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22226%2FFHD%2Fskyatlantic.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AoOU%2FfBvAa%2FzmRM0oDJ9hmQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Serie HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23684%2FFHD%2Fskyserie.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A8eK8HGp2tChF0XthH6b%2B1A%3D%3D%2Ckid%3Aheader%29)
- [Comedy Central SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F22404%2Fcomedycentral.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AoZrXxaJtFYRJHn%2FTLivIPw%3D%3D%2Ckid%3Aheader%29)
- [History HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21513%2FFHD%2Fhistory.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AD9a%2Bytw3P9Z%2BDIFKzWk9mA%3D%3D%2Ckid%3Aheader%29)
- [Sky Investigation HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23686%2FFHD%2Fskyinvestigation.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AqR5ICKNjqqgfMaQ31pW9Og%3D%3D%2Ckid%3Aheader%29)
- [Crime Investigation HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21249%2FFHD%2Fcrimeinvestigation.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AaXfBxRzj5%2FKLrEGIVN8pgQ%3D%3D%2Ckid%3Aheader%29)
- [MTV HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21763%2FFHD%2Fmtvnext.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3Av7D53XuisAWDSl27Yp5qbg%3D%3D%2Ckid%3Aheader%29)
- [Sky Arte HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22074%2FFHD%2Fskyarte.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AjMh1aFf0YGSk2wyk5oAITw%3D%3D%2Ckid%3Aheader%29)
- [Sky Documentaries HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23697%2FFHD%2Fskydocumentaries.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AE9yGiu5cwbcO9Oot%2FIc2hg%3D%3D%2Ckid%3Aheader%29)
- [Sky Nature HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22695%2FFHD%2Fskynature.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A7GEnuIsetJ93mDW7T6Y%2FSA%3D%3D%2Ckid%3Aheader%29)
# Cinema
- [Sky Cinema Uno HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22202%2FFHD%2Fcinemauno.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AdDCTX0ChL%2Bt8IP56S9iXiQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema Comedy HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22030%2FFHD%2Fcinemacomedy.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3Aa2W2%2B9MFbIrwrd%2BhkFni5A%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema Action HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22206%2FFHD%2Fcinemaaction.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3ADcHLmPXq%2BR8Q8Ug00IBTMA%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema Due HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22564%2FFHD%2Fcinemadue.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A2yqrLGxWJpGMiaqfbv7Q1w%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema CollectionHD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22204%2FFHD%2Fcinemacollection.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AyZTYUda%2F%2FbLmkbLv%2FhDoFg%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema Family HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22255%2FFHD%2Fcinemafamily.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AvbNRBz5MRr2YEkiwiVC1ng%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema Suspense HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22047%2FFHD%2Fcinemasuspense.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AXkUOgTyufhzW5DEnHNvrew%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema Romance HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22231%2FFHD%2Fcinemaromance.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A2rNh5inSdLCgIRlAf86K%2Bw%3D%3D%2Ckid%3Aheader%29)
- [Sky Cinema Drama HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22769%2FFHD%2Fcinemadrama.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AymZPJ9d9jOEj8dCUSNaDEQ%3D%3D%2Ckid%3Aheader%29)
# Sport
- [Sky Sport 24 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23035%2FFHD%2Fskysport24.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AA87z6V8R8Cks3ffw1CvyFg%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport Uno HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23023%2FFHD%2Fskysportuno.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AyNntfeTGYrV0DLeLNnSmIQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport F1 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23478%2FFHD%2Fskysportf1.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AOX7oxqSNkzRFL%2F1n1uWrUA%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport MotoGP HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23483%2FFHD%2Fskysportmotogp.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AvtLIUbVyTSPJPnjuRwiUUg%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport Calcio HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23209%2FFHD%2Fskysportseriea.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AmrOOPe96Ttb4NtF2B5Z41Q%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport Football HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21248%2FFHD%2Fskysportfootball.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AOkCzHhXYPNA3pjSoaDpEVg%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport Tennis HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22559%2FFHD%2Fskysporttennis.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AoOXQKrJJqswp9%2FLCwSdbhQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport Arena HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23024%2FFHD%2Fskysportarena.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3ANEwvNLpiz0yns6jtD44oHA%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport NBA HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21764%2FFHD%2Fskysportnba.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A1rpVZgBs%2FZkNNLu4Ah1S%2BA%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport Golf HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23768%2FFHD%2Fskysportcollection.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AmIvRkftFVAmTtF1iryXARg%3D%3D%2Ckid%3Aheader%29)
- [Eurosport 1 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F213073%2FFHD%2Feurosport.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AfJ5z5UGLXaTDZ%2BagKkWL8A%3D%3D%2Ckid%3Aheader%29)
- [Eurosport 2 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21150%2FFHD%2Feurosport2.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AWVq7spCMtJXllsnRUYKIUQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 251 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21917%2FFHD%2Fskysport251.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A%2BzBSk7dZtCYSI9lXDusRhg%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 252 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22951%2FFHD%2Fskysport252.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3Awq3aCuiP%2BVqkv6HWK6dZSA%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 253 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23233%2FFHD%2Fskysport253.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AQ2E2tgRa6Yb7V4qiZbwm2Q%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 254 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21234%2FFHD%2Fskysport254.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AoTOtqPrAo8LugwmapjcamA%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 255 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22910%2FFHD%2Fskysport255.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A75vhUYXe6xpMF%2Ffc059TRQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 256 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F23912%2FFHD%2Fskysport256.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AlmzuROciyRtKF%2FJrKvo0tQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 257 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21775%2FFHD%2Fskysport257.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A2rYZGV6Wj6kFBZ9oi6weUg%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 258 HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F22772%2FFHD%2Fskysport258.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3ARZVawdEQJigjgI74993x2Q%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 259 SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F23613%2Fskysport259.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AXCu0k%2FSdnFAQJ4fkk67N9Q%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 260 SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F23615%2Fskysport260.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3Abj19gX8a1GIdVs%2B%2FlKPYNQ%3D%3D%2Ckid%3Aheader%29)
- [Sky Sport 261 SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F21617%2Fskysport261.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3Agclrpgcegz33RIBI8e6oQg%3D%3D%2Ckid%3Aheader%29)
# Kids
- [Cartoon Network HD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-hd-nowtv.skycdn.it%2F21258%2FFHD%2Fcartoonnetwork.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A%2BE7U8otme6pKtSYhd96vSw%3D%3D%2Ckid%3Aheader%29)
- [Nickelodeon SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F21320%2Fnickelodeon.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3Ay4vlovji1rB0C3RnaNXlhw%3D%3D%2Ckid%3Aheader%29)
- [DeAKids SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F22460%2Fdeakids.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A6AXNiKf22jLpe4KAfrvARw%3D%3D%2Ckid%3Aheader%29)
- [Nick Jr. SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F22424%2Fnickj.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3A2%2B453OB9fBy%2BJP%2BlK3TkoQ%3D%3D%2Ckid%3Aheader%29)
- [Boomerang SD](https://bitmovin.com/demos/stream-test?format=smooth&manifest=https%3A%2F%2Fhss-live-nowtv.skycdn.it%2F21367%2Fboomerang.isml%2FManifest&drm=playready&license=https%3A%2F%2Ftest.playready.microsoft.com%2Fservice%2Frightsmanager.asmx%3Fcfg%3D%28contentkey%3AspjYAFY24jUKUQTPicnTGg%3D%3D%2Ckid%3Aheader%29)
