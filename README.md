<h1 align="center">Ödüllü Subspace Testneti Kurulum Rehberi

## Selamlar, bugün ödüllü Subspace Gemini 2 Testneti için node kuracağız. Ödül için bazı şartlar var, detayları aşağıda açıklıyorum. Sağ üstten yıldızlayıp forklamayı unutmayalım. Sorularınız olursa: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/191612639-038662d6-472b-401a-b7a3-4ce7ead249be.png)

## Minimum sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Testnet | 2          | 4         | 150GB  |


## Subspace için önemli linkler:
- [Website](https://subspace.network/)
- [Explorer(ımsı) Telemetry](https://telemetry.subspace.network/#list/0x43d10ffd50990380ffe6c9392145431d630ae67e89dbc9c014cac2a417759101)
- [Subscan](https://subspace.subscan.io/)
- [Twitter](https://twitter.com/NetworkSubspace)
- [Discord](https://discord.gg/APGKbgn5nT)

# Detaylara göz atalım.

- Ödül dağıtımı için toplam node sayısının 25k'dan fazla olması gerekiyor. Güncel node sayısını [Telemetry](https://telemetry.subspace.network/#list/0x43d10ffd50990380ffe6c9392145431d630ae67e89dbc9c014cac2a417759101) üzerinden öğrenebilirsiniz.

![image](https://user-images.githubusercontent.com/101462877/191612980-d6027b1a-4d49-4292-91c9-9c78548169ca.png)

- Node sayısının 25k'yı geçtiği durumda dağıtılacak ödül için belirli dönüm noktaları yine yukarıdaki görselde belirtilmiş.

- Eğer ödül dağıtımı gerçekleşirse, ödül 0.5 tSSC üzerinde token biriken tüm adreslere eşit dağılacak.

# Kuruluma başlayalım. Öncelikle Subspace adresine ihtiyacımız olacak.

[Polkadot](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Feu-1.gemini-2a.subspace.network%2Fws#/accounts) sayfasına gidiyoruz. Aşağıdaki görselleri takip ederek hesap oluşturuyoruz.
![image](https://user-images.githubusercontent.com/101462877/191613967-2481ff35-7f81-4cca-b9b9-e1fed47676d8.png)

Hesap için bize verdiği kelimeleri bir yere not ediyoruz.

![image](https://user-images.githubusercontent.com/101462877/191614057-75431d2f-eaf9-4e22-982b-9a5418fdcf43.png)

Kalan aşamaları da next next dedikten sonra aşağıdaki görselde gördüğünüz gibi hesabımız oluştu.

![image](https://user-images.githubusercontent.com/101462877/191614351-435cd3a6-6ffd-4936-afb0-751882b98946.png)


# Terminalimize geliyoruz ve tek kod script'i yapıştırıyoruz.

```
wget -O subspace.sh https://raw.githubusercontent.com/thisislexar/Subspace-Gemini-2-Odullu-Testnet/main/subspace.sh && chmod +x subspace.sh && ./subspace.sh
```

# Node kurduğumuz sunucuda daha öncesinde Subspace node'u çalıştırmadıysak (ki çoğumuz muhtemelen çalıştırmamıştır) bu kısımda `n` yazıp enterlıyoruz.

![image](https://user-images.githubusercontent.com/101462877/191615072-9090c2f8-b067-41c7-b487-20fc074022cd.png)

# Bize Subspace adresimizi soruyor, az önce oluşturduğumuz hesabın adresini yapıştırıyoruz.

![image](https://user-images.githubusercontent.com/101462877/191615296-3f6a8a58-13cc-444d-8737-2d66e73f4cac.png)


![image](https://user-images.githubusercontent.com/101462877/191615366-a8821c1f-2e07-4a13-a9a8-f28f17595892.png)


# Node ismimizi giriyoruz.

![image](https://user-images.githubusercontent.com/101462877/191615539-9c186e55-f0fb-42fc-b92d-7ece60801c24.png)


# Görseldeki formattaki gibi plot size giriyoruz. Maximum 100GB girebiliyorsunuz. Sunucunuzda plot size'ın dışında yaklaşık 50GB boşluk bırakın. Örneğin, sunucunuz 125 GB ise plot size'a 75GB yazabilirsiniz.

![image](https://user-images.githubusercontent.com/101462877/191617405-88f382fe-62ee-4fdf-b02b-09b479e52f2a.png)

# `y`'ye basarak bilgileri onaylıyoruz.

![image](https://user-images.githubusercontent.com/101462877/191617534-c5e1a46c-c5a6-40d5-b46c-4e458d2bda5a.png)

# Node'umuzu başarıyla kurduk, görseldeki kutu içerisindeki komutları kolay ulaşım açısından bir kenara not edebilirsiniz.

![image](https://user-images.githubusercontent.com/101462877/191617838-956cfeef-7a26-4e9e-b14e-89c1af007acf.png)


# Loglarımızın akışını kontrol edelim ve node'umuzun [Telemetry](https://telemetry.subspace.network/#list/0x43d10ffd50990380ffe6c9392145431d630ae67e89dbc9c014cac2a417759101)'de görünüp görünmediğine bakalım.

![image](https://user-images.githubusercontent.com/101462877/191618055-08b15f5e-9c33-4c07-a9c3-5b8ca9ce64ec.png)

# Sorularınız ve merak ettikleriniz için: [LossNode Chat](https://t.me/LossNode)

# Node silmek için: 

```
rm -rf ~/.local/share/subspace*
rm -rf /etc/systemd/system/subspace*
rm -rf /usr/local/bin/subspace*

rm -r /root/.local/share/subspace-farmer
rm -r /root/.local/share/subspace-node
```
