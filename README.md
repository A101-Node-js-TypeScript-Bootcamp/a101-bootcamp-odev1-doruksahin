--- Javascript ve Typescript arasındaki farklar
1. TS compile edilir, JS interprete edilir. TS compile edildiği için hatalar compile time'da görülebilir.
JS'te bu problem için eslint gibi toollar kullanılmaktadır.
2. TS static typing, JS dynamic typing kullanır. TS'in bu özelliği ile kod daha hızlı çalışır. Kod okumak daha kolay olur. Fakat dynamic typing'in de işe yaradığı nadir durumlar vardır. Kod tekrarını önler.
3. TS'in debug edilmesi kolaydır, JS'in yazımı kolaydır.
4. TS yazabilmek için JS bilinmelidir. Bu da TS'in dezavantajıdır.
5. TS önce JS koduna dönüştüğü için TS bir miktar daha yavaş çalışır.
6. TS, büyük web uygulamaları yazılırken kullanıldığında çok işlevlidir, karmaşıklığı önler;
JS ise küçük projelerde, hızlı işlerde işe yarar.

--- Node server nasıl ayağa kaldırılır?
1. Node projesi oluşturmak için package.json'a ihtiyacımız vardır. Gerekli formatın oluşturulması için NPM'den yardım alırız.
npm init komutu ile yeni projemizi oluştururuz. Burada npm'in sorduğu alanları doldururuz ve package.json oluşur.
2. npm install express ile express kütüphanesini indirebiliriz. Şart değil fakat express api yazma konusunda kolaylık sağlar.
3. Bir dosyaya aşağıdaki kodlar yazılır ve npm start komutunu çalıştırırsak node serverımız localhost'ta 3000 portunda ayağa kalkacaktır. 

$$$$
const express = require('express')
const app = express()
const port = 3000
app.listen(port, () => console.log(`Example app listening on port ${port}!`))
app.get('/', (req, res) => res.send('Hello World!'))
$$$$

