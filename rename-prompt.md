You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "KS REALTORS | ABOUT US",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "KS REALTORS | CONTACT US",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/827fd34f9214e869c8b614f913aef7d5.css",
    "context": {
      "path": "css/827fd34f9214e869c8b614f913aef7d5.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/9297b3c7dd47db40d42fafefe753d3a2.css",
    "context": {
      "path": "css/9297b3c7dd47db40d42fafefe753d3a2.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/02472629160fe58d93e3251d6bed1550.webp",
    "context": {
      "refs": [
        {
          "alt": "251fe2d760124481b2603a68c3b7f86b",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/02668c7b6b2ff0efa2ee13d1529002d3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/068926d48a895527ec3ea20460c455cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0b2d9768e7c1efe03cc896895daa8ae7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e2f8b204bce9dbee30025880c7164cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e71f49df158184f3a2ed58fd8a60c10.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0096",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12b5c9c96cb718c733ede11498e23d07.webp",
    "context": {
      "refs": [
        {
          "alt": "FOUNDATION STONE LAYING CEREMONY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/166c09d20fa3417ae156989e8fe19e16.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1aabbcb82b5493c0843c64a3ed49c381.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/246a4a070126f772920d3f6daadfaf97.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0111",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/248c11f5fc9ff9dda0f025bf90ca1850.webp",
    "context": {
      "refs": [
        {
          "alt": "BASEMENT SLAB",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2614820e1d13dfb3834ee6bb97def76f.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG3862",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d7c80741cfa5b9007fefa6c8d915e6b.webp",
    "context": {
      "refs": [
        {
          "alt": "PHOTO20180630153004",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e738ae1bcdd8d709fc5e836b05d625f.webp",
    "context": {
      "refs": [
        {
          "alt": "16",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f234baf73dca4d2e74124d751e95152.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31c8a63d3502efdeb208b3157e84f33c.webp",
    "context": {
      "refs": [
        {
          "alt": "WORK AREA-MOCK APPT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33efb0c21a9a0a18dbbbb9c6dec6c43d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34c3a9d6633919e91d2fe3660a20f6b8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/36b90098ce9f00ea72d4d617fbe0aae5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3818213b0d41c566b9d7ae0ade2125ed.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0107",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ca1285421ae30a5d1a1d6d433c61a70.webp",
    "context": {
      "refs": [
        {
          "alt": "12",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3fea84c263f86c4016732d8f2cb1db3a.webp",
    "context": {
      "refs": [
        {
          "alt": "13",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/421a236dcd4ee03ce27eab63003e6e7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4431946587394f4e04558f36cdbc16df.webp",
    "context": {
      "refs": [
        {
          "alt": "REGALIA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46af20ef9166743fce958b07470c936f.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0083",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c1c50b3aa092fa56375588bed6dc5fb.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9258",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e4a2ec538e39cbb2c97c2d419ffb270.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9272",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/56845f5c66d07de1beab81fee0d778ce.webp",
    "context": {
      "refs": [
        {
          "alt": "2",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bcaeb74b55be9956e8414e68352489b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/5e57df6c5638acce81d423fa0ba3a8dd.webp",
    "context": {
      "refs": [
        {
          "alt": "Vision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/61cde662636d666c5d36a541d88c79aa.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0106",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/681cac1c2ef49239d70eaabec4edd28e.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0110",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a8f28b62ec3e3db50087f10f143cc2c.webp",
    "context": {
      "refs": [
        {
          "alt": "Mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fa649159e8831fcd30974a523e897b8.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0090",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/763d9a7e7284c0b7a7212982d8054bb9.webp",
    "context": {
      "refs": [
        {
          "alt": "14",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/778b47341566d08a0129a0842efe970d.webp",
    "context": {
      "refs": [
        {
          "alt": "9",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/77a4d2e2040064326701936a18d9d750.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7a97fcc5102760dc15357c815e77c10d.webp",
    "context": {
      "refs": [
        {
          "alt": "KS REALTORS PVT LTD is an integrated real estate developer focused on premium developments with resi",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ede181e20d959fe37a648918c65cc75.webp",
    "context": {
      "refs": [
        {
          "alt": "Regalia | 2 & 3 BHK luxurious apartments. Sizes ranging from 1165 sq.ft. to 2040 sq.ft.. They are eq",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81c418e7398df3b4ad9ce0c5ea3081f7.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0097",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83746d159f3269faff94407df8da1b97.webp",
    "context": {
      "refs": [
        {
          "alt": "REGALIA APARTMENTS- MOCKUP- VAZUDACAUD, TRIVANDRUM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/859c51bf4ca45c85f58a00e13a8542dd.webp",
    "context": {
      "refs": [
        {
          "alt": "BRILLIANTLY CONCEPTUALIZED LUXURY RESIDENCES",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88650f0ba9d5dd87b67b6b0af22e5859.webp",
    "context": {
      "refs": [
        {
          "alt": "4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88a4f99ad30173b670e8fc9b5104a34f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a2ab4e023ea454b4a356b3578d5f49e.webp",
    "context": {
      "refs": [
        {
          "alt": "FOUNDATION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a3b63c04e7715304195392107d18474.webp",
    "context": {
      "refs": [
        {
          "alt": "5",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a790e536310bccc2c01c820e0f8ae43.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e83227a30e858c59bf1c65d2231517b.webp",
    "context": {
      "refs": [
        {
          "alt": "10",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f7320a487346ea5858348e8891bb2ff.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9334fa859151689325129403f4a888e9.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0095",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/95f178a1b3f3cef700f1acb7178d2ff2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/984e443e319192ac74b88ba9d5725031.webp",
    "context": {
      "refs": [
        {
          "alt": "REGALIA APARTMENTS- MOCKUP- VAZUDACAUD, TRIVANDRUM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98bbff518ef8b4a4d7fc15f12476dc4a.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0093",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9acd2b725cceca4beb82c1b718a52a86.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9cc5489e6269d778d6d21c7b174b9b65.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0e4705e7ad1ba50101ebf536d9fc1f2.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0094",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a112f1d0ec5e700ce2014c7f3d95beb8.webp",
    "context": {
      "refs": [
        {
          "alt": "9",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a3c15f0572ec94d67234194f81fee621.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a566a1a24cb44962c5e2ee713a8525b1.webp",
    "context": {
      "refs": [
        {
          "alt": "REGALIA APARTMENTS- MOCKUP- VAZUDACAUD, TRIVANDRUM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a69210e1f86096655ccb57c174d89c64.webp",
    "context": {
      "refs": [
        {
          "alt": "7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aed1273aebf68d9f6a9cfb3bddd130bf.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0084",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b11ae60209a84075bca0db123180d98a.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9251",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b325a96e3f6d0a01a6346a99ca86beed.webp",
    "context": {
      "refs": [
        {
          "alt": "PILING WORKS IN PROGRESS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4aaa0d56240f290bef3585e436e9201.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4c492668dc24bd450b8d7733c57d04e.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0105",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9a3d1a81918ea63c96a1568c0f0733b.webp",
    "context": {
      "refs": [
        {
          "alt": "PILING WORKS IN PROGRESS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf9e3dfbf823422624571e413af1dd22.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9255",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1fd5e638d0512e866be8538f5043eaf.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0092",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c66548e3ba5f9107b09855486f7ecbc5.webp",
    "context": {
      "refs": [
        {
          "alt": "6",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6e0e86549c967a25986df8fbf1652fa.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0108",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce4575b7c771da132d3ea78567a02262.webp",
    "context": {
      "refs": [
        {
          "alt": "APPROVAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d156f8bf8f4e0ab593fa7daf3213de58.webp",
    "context": {
      "refs": [
        {
          "alt": "REGALIA APARTMENTS- MOCKUP- VAZUDACAUD, TRIVANDRUM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5d1823fe1fcd352082ce1413d211223.webp",
    "context": {
      "refs": [
        {
          "alt": "Corporate Values",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db6570562fddc45e533960dcd176f9db.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0100",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ddc55f543892a2c461e1e634cacc09ac.webp",
    "context": {
      "refs": [
        {
          "alt": "REGALIA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dfe744b8ef941450128bf8c6b23b6072.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ecce67a987093970fccec10665751a57.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG0086",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee8cebda3dcad4c4a9a53798114b8814.webp",
    "context": {
      "refs": [
        {
          "alt": "15",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f258beb83a8293b52f7c0ad0887e9cc2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f770d1bd367ec5651a9da63c730a1f1b.webp",
    "context": {
      "refs": [
        {
          "alt": "We strongly believe that delivering projects is the first step in our long-lasting journey with our ",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbad8898c703187eef422010d0d6c78b.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG3866",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fdfe14f96adfdd29f8c73a40a469a6f5.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG9256",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fff0b152429676deaf415f210a13643b.webp",
    "context": {
      "refs": [
        {
          "alt": "REGALIA APARTMENTS- MOCKUP- VAZUDACAUD, TRIVANDRUM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "KS REALTORS | BUILDING YOUR DREAMS | REGALIA | BRILLIANTLY CONCEPTUALIZED LUXURY RESIDENCES | HOME",
      "first_heading": "KS REALTORS"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "js/fbd713fde01d36f8fdfc5482ae0d87d7.js",
    "context": {
      "path": "js/fbd713fde01d36f8fdfc5482ae0d87d7.js"
    }
  },
  {
    "path": "projects.html",
    "context": {
      "title": "KS REALTORS | REGALIA",
      "first_heading": "FLOOR UNIT SUMMARY"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.