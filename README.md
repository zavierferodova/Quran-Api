<p align="center">
<img alt="node-current" src="https://img.shields.io/node/v/jest">
    <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/zavierferodova/Quran-Api">
    <a href="https://github.com/zavierferodova/Quran-Api/blob/master/LICENSE">
    	<img alt="GitHub" src="https://img.shields.io/github/license/zavierferodova/Quran-Api">
    </a>
    <br>
    <br>
    <a href="https://quran-data.vercel.app/">
      <img alt="Website" src="https://img.shields.io/website?label=vercel&down_message=offline&up_message=online&url=https%3A%2F%2Fquran-data.vercel.app%2F">
    </a>
</p>



<hr />

This project is made for developers who want to develop Islamic applications. besides that this project also aims to be a charity for developers who develop applications with this API, especially me and the developers from the data sources that I get.

## Content

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage/Endpoint](#usageendpoint)
- [Sample Apps](#sample-apps)
- [Data Resources](#data-resources)
- [Quran Fonts](#quran-fonts)



### Introduction

This API was created to make it easier for developers to develop Islamic applications. There are several different recitations so that developers can create dynamic audio. The data used in the development of this API is taken from several different [sources](#data-resources), both from existing APIs and from scraping results.

This API was created using the [Express Web Application Framework](https://expressjs.com/) and several additional libraries that you can see in the `package.json` file.

**File Structure :**

```
Quran-Api
├── __test__/
├── data/
│	├── imam.json
│	└── quran.json
├── server/
|	├── app.js
|	├── controller.js
|	├── middleware.js
|	└── routes.js
├── static/
├── util/
├── package.json
└── package-lock.json

```



[⬆️ Back to Top](#content)



### Installation

There are several different ways to do the installation, you can use whichever you like

- **Localhost**

  ```bash
  # clone the repository
  > git clone https://github.com/zavierferodova/Quran-Api.git quran-api
  
  # change directory
  > cd quran-api
  
  # install all packages from package.json
  > npm install
  
  # now, you can start it
  > npm start
  ```
  

- **Vercel Deploy**

  click the deploy button below. Register your own [vercel](https://vercel.com) account

  [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/git/external?repository-url=https%3A%2F%2Fgithub.com%2Fzavierferodova%2FQuran-Api)



**Note :** if you have problems with installation, feel free to create an issue.

[⬆️ Back to Top](#content)



### Usage/Endpoint

---

**Base** : https://quran-data.vercel.app/

**Alternative** : -

---

Some of these API endpoints that you can access, start the application on your local computer or for a demo, you can go to the following link [Qur'an Endpoint](http://quran-data.vercel.app/)

- **/imam/:id**

  Displays list of imam

  *params* :

  `[Optional] id : Spesific imam id`

  *query* :

  `-`

  *example* :

  ```bash
  # display all imam
  > curl -v -H "Content-Type: application/json" \
  > http://quran-data.vercel.app/imam
  
  # display spesific imam
  > curl -v -H "Content-Type: application/json" \
  > http://quran-data.vercel.app/imam/2
  ```

- **/quran/:surah/:ayah?imamId=**

  Display list of surah in qur'an

  *params* :

  `[Optional] surah : spesific surah in qur'an` 

  `[Optional] Ayah : Spesific Ayah in qur'an surah`

  *query* :

  `[Optional] imamId : Spesific imam id, get it from /imam`

  *example :*

  ```bash
  # show all qur'an surah (without ayah)
  > curl -v -H "Content-Type: application/json" \
  > http://quran-data.vercel.app/quran
  
  # show spesific qur'an surah (with ayah)
  > curl -v -H "Content-Type: application/json" \
  > http://quran-data.vercel.app/quran/12
  
  # show spesific ayah in a surah
  > curl -v -H "Content-Type: application/json" \
  > http://quran-data.vercel.app/quran/12/4
  
  # note :
  #	you can add the ?imamId= query wherever you want,
  # e.g :
  #	/quran?imamId=2
  #	/quran/12?imamId=10
  #	/quran/12/4?imamId=6
  ```

  

  **Note :** if you have problems with Usage/Endpoint, feel free to create an issue.



[⬆️ Back to Top](#content)



### Sample Apps

You can get inspired and learn from the sample apps below that use this API

- (Your Apps)



### Data Resources

all the data in this api is obtained from several sources below

- [Kemenag RI](https://quran.kemenag.go.id/)
- [quran/quran.com-api](https://github.com/quran/quran.com-api)
- [sutanlab/quran-api](https://github.com/sutanlab/quran-api)
- [islamic-network/api.alquran.cloud](https://github.com/islamic-network)
- [quranicaudio.com](https://quranicaudio.com/about)
- [everyayah.com](https://everyayah.com/)



[⬆️ Back to Top](#content)


### Quran Fonts

Some quran fonts for you projects

- [PDMS Saleem QuranFont](https://www.maisfontes.com/pdms-saleem-quranfont)
- [Al Qalam Quran Majeed](https://arabicfonts.net/fonts/al-qalam-quran-majeed-web-regular)
- [me_quran](https://urdufonts.net/fonts/me_quran-regular)
- [noorehidayat](https://urdufonts.net/fonts/noorehidayat-regular)
- [Summary](http://quran.mursil.com/Web-Print-Publishing-Quran-Text-Graphics-Fonts-and-Downloads/fonts-optimized-for-quran)
- [Arabic Fonts](https://arabicfonts.net/fonts)



[⬆️ Back to Top](#content)



Thank you