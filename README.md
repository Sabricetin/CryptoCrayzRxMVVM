### Kripto Para Uygulaması (CryptoCrayzRxMVVM)

Bu Swift uygulaması, bir `UITableView` kullanarak kripto para birimlerini listeleyen ve kullanıcıların bu para birimlerinin fiyatlarını görüntüleyebileceği bir iOS uygulaması oluşturur. Kod, MVVM (Model-View-ViewModel) tasarım desenini kullanır ve RxSwift ile reaktif programlama ilkelerini uygular.

## Özellikler

- **Veri Kaynakları:**
  - `cryptos`: Kripto para birimlerinin isimlerini ve fiyatlarını tutar.
  - `error`: Uygulama sırasında oluşabilecek hata mesajlarını tutar.
  - `loading`: Verilerin yüklendiğini gösterir.

- **Kullanıcı Arayüzü:**
  - `tableView`: Kripto para birimlerini listelemek için kullanılır.
  - `indicatorView`: Veri yükleme sırasında gösterilen yükleme göstergesi.

## View Did Load

- `tableView` için `delegate` atanır.
- ViewModel ile kullanıcı arayüzü arasındaki bağlamalar (bindings) kurulur.
- Veriler `CryptoViewModel` aracılığıyla indirilir ve tabloya yüklenir.

## UITableViewDataSource

- `tableView(_:numberOfRowsInSection:)`: Satır sayısını, kripto para birimlerinin sayısı olarak döner.
- `tableView(_:cellForRowAt:)`: Her bir hücreyi, ilgili kripto para biriminin adı ve fiyatı ile doldurur.

## UITableViewDelegate

- `tableView(_:didSelectRowAt:)`: Bu uygulamada, bir satırın seçimi sonrası bir işlem yapılmaz; ancak detay görüntüleme gibi ek özellikler eklenebilir.

## Custom Table View Cell

- `CryptoTableViewCell`: Her bir kripto para birimi için, adı ve fiyatını gösteren özel bir hücre yapılandırılmıştır. Hücredeki etiketler (labels), modelden gelen verilerle güncellenir.

## Ekran Görüntüleri


![yeni gif](https://github.com/user-attachments/assets/43980052-2fa0-48be-84a8-9eaa099e62ca)


## Kullanım

- Uygulamayı başlattığınızda, ana ekranda kripto para birimlerinin listesini göreceksiniz.
- Liste otomatik olarak güncellenir ve kripto para birimlerinin güncel fiyatlarını gösterir.
