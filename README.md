<p align="center">
  <img src="https://user-images.githubusercontent.com/5600341/27505816-c8bc37aa-587f-11e7-9a86-08a2d081a8b9.png" height="280px">
  <p align="center">Tarayıcıda ve sunucu içinde PDF dosyaları oluşturmak için kullanabileceğiniz, React renderer<p>
  <p align="center">
    <a href="https://www.npmjs.com/package/@react-pdf/renderer">
      <img src="https://img.shields.io/npm/v/@react-pdf/renderer.svg" />
    </a>
    <a href="https://travis-ci.org/diegomura/react-pdf">
      <img src="https://img.shields.io/travis/diegomura/react-pdf.svg" />
    </a>
    <a href="https://github.com/diegomura/react-pdf/blob/master/LICENSE">
      <img src="https://img.shields.io/github/license/diegomura/react-pdf.svg" />
    </a>
    <a href="https://github.com/prettier/prettier">
      <img src="https://img.shields.io/badge/styled_with-prettier-ff69b4.svg" />
    </a>
    <a href="https://app.fossa.com/projects/git%2Bgithub.com%2Fdiegomura%2Freact-pdf?ref=badge_shield" alt="FOSSA Status"><img src="https://app.fossa.com/api/projects/git%2Bgithub.com%2Fdiegomura%2Freact-pdf.svg?type=shield"/></a>
  </p>
</p>

## Kayboldun galiba?

Bu paket React JS kullanarak yeni PDF dosyası _oluşturmak_ için kullanılır. Eğer var olan PDF'i görüntülemek için bir şey arıyorsanız: [react-pdf](https://github.com/wojtekmaj/react-pdf).

## Kurulum
```sh
yarn add @react-pdf/renderer
```

## Nasıl çalışır?

```jsx
import React from 'react';
import { Document, Page, Text, View, StyleSheet } from '@react-pdf/renderer';

// Create styles
const styles = StyleSheet.create({
  page: {
    flexDirection: 'row',
    backgroundColor: '#E4E4E4'
  },
  section: {
    margin: 10,
    padding: 10,
    flexGrow: 1
  }
});

// Create Document Component
const MyDocument = () => (
  <Document>
    <Page size="A4" style={styles.page}>
      <View style={styles.section}>
        <Text>Section #1</Text>
      </View>
      <View style={styles.section}>
        <Text>Section #2</Text>
      </View>
    </Page>
  </Document>
);
```

### DOM'da 'Web' render.
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import { PDFViewer } from '@react-pdf/renderer';

const App = () => (
  <PDFViewer>
    <MyDocument />
  </PDFViewer>
);

ReactDOM.render(<App />, document.getElementById('root'));
```

### `Node.` ile bir dosyaya kayıt etme.
```jsx
import React from 'react';
import ReactPDF from '@react-pdf/renderer';

ReactPDF.render(<MyDocument />, `${__dirname}/example.pdf`);
```

## Katkıda bulunanlar

Bu proje, katkıda bulunan tüm insanların sayesinde varlığını sürdürmektedir. Katkıda bulunmayı mı düşünüyorsunuz? Lütfen [[katkıda bulunmak]](https://github.com/diegomura/react-pdf/blob/master/.github/CONTRIBUTING.md) hakkındaki dökümanımıza göz atın. Geliştirme ortamını nasıl kuracağınız ve nasıl kod göndereceğiniz hakkında daha fazla bilgi alabilirsiniz.

<a href="https://github.com/diegomura/react-pdf/blob/master/.github/CONTRIBUTING.md"><img src="https://opencollective.com/react-pdf/contributors.svg?width=890" /></a>

## Sponsorlar

Thank you to all our sponsors! [[Become a sponsors](https://opencollective.com/react-pdf#sponsors)]

<a href="https://opencollective.com/react-pdf#sponsors" target="_blank"><img src="https://opencollective.com/react-pdf/sponsors.svg?width=890"></a>

## Destekçiler

Tüm destekçilerimize teşekkür ederiz! [[Destekçi ol](https://opencollective.com/react-pdf#backer)]

<a href="https://opencollective.com/react-pdf#backers" target="_blank"><img src="https://opencollective.com/react-pdf/backers.svg?width=890"></a>

## Lisans

MIT © [Diego Muracciole](http://github.com/diegomura)

[![FOSSA Durumu](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fdiegomura%2Freact-pdf.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fdiegomura%2Freact-pdf?ref=badge_large)

---
![](https://img.shields.io/npm/dt/@react-pdf/renderer.svg?style=flat)
