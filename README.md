
# Readme


## Goal

Scientific Research and Development has become an increasingly important factor in the development of any nation. In any country, scientific research and technology support effective policy-making by the government, improve the quality of life of its people, strenghten the economy by improvising and streamlining business, and boost health as well as overall well being. In this project, I am exploring how the push towards research has changed around the world over the last decade. And if the greater expenditure on research and development by the government has resulted in increased high technology exports, higher publications and journal articles, more patents, more reserchers, and more industrial design applications. A positive correlation between R&D expenditure and other indicators representing scientific development will strengthen the case of growth in research not being just a random phenomenon. Although there are many social, economic, cultural, and political factors that contribute to research in any country, policy makers can be assured that more investment in R&D does indeed positively boost research and its implied economic benefits. 

I chose the World Development Indicators (States and Markets) dataset by the World Bank for my exploratory analysis.


According to [World Bank](http://datatopics.worldbank.org/world-development-indicators/), The World Development Indicators is "a compilation of relevant, high-quality, and internationally comparable statistics about global development and the fight against poverty. The database contains 1,600 time series indicators for 217 economies and more than 40 country groups, with data for many indicators going back more than 50 years."

It has 6 data themes:
1. Poverty and Inequality
2. People 
3. Environment
4. Economy
5. States and Markets
6. Global Links

Out of these, I will be mainly focusing on the theme "States and Markets" for indicators like Research and development expenditure (% of GDP), Scientific and technical journal articles, ICT goods exports (% of total goods exports), Patent applications (residents), and Time required to start a business (days).

## Data

The [Developer Documentation](https://datahelpdesk.worldbank.org/knowledgebase/topics/125589) provides various APIs to access the datasets.

Out of the 6 themes listed [here](http://datatopics.worldbank.org/world-development-indicators/), I downloaded the following datasets containing CSV files for the theme [States and Markets](http://datatopics.worldbank.org/world-development-indicators/themes/states-and-markets.html). I may utilize the APIs later if I require more control and customizations. 

#### States and Markets
According to World Bank, States and markets statistics focus on "private sector development, including entrepreneurship and finance; infrastructure development; and public policies and institutions that affect the economy. Many of these topics are also part of the Sustainable Development Goals."

According to the documentation, Wbdata is a simple python interface to find and request information from the World Bank’s various databases, either as a dictionary containing full metadata or as a pandas DataFrame. 
Currently, wbdata wraps most of the World Bank API, and also adds some convenience functions for searching and retrieving information. For ex., wbdata.get_dataframe(), wbdata.search_countries(). Documentation for wbdata can be found [here](https://wbdata.readthedocs.io/en/latest/).

Again, there are datasets for various economic indicators. Currently, I have obtained the dataset for the following indicators for all countries using Wbdata API from 2005 till 2015:


| Indicator Name                                             | Indicator Code   |
|--------------------------------------------------------------------------------------------|------------------|
|Researchers in R&D (per million people)                                                         | SP.POP.SCIE.RD.P6|
|High-technology exports (current USD)                                                           | TX.VAL.TECH.CD   |
|Government expenditure on education, total '(% of GDP)'                                         | SE.XPD.TOTL.GD.ZS|
|Educational attainment, Doctoral or equivalent, population 25+, total (percentage) (cumulative) | SE.TER.CUAT.DO.ZS |
|Research and development expenditure (percentage of GDP)                                        | GB.XPD.RSDV.GD.ZS |
|Patent applications, residents                                                                  | IP.PAT.RESD       |
|GDP per capita (current US$)                                                                    | NY.GDP.PCAP.CD    |
|Scientific and technical journal articles | IP.JRN.ARTC.SC |
|High Technology Exports|TX.VAL.TECH.CD|
|Industrial Design Applications| IP.IDS.RSCT|
|ICT goods exports| TX.VAL.ICTG.ZS.UN|

   


## Analysis

#### Research questions:

* **RQ 1.** 10 countries with the highest and lowest Research and Development expenditure (% of GDP) in last 10 years.
* **RQ 2.** How has R&D expenditure (% of GDP) changed over the last 10 years for these countries?
* **RQ 3.** Is there a relationship between R&D expenditure and other Science and innovation indicators like researchers per million people, Scientific and technical journal articles, ICT goods and high technology exports, high-technology exports (current USD), etc.
* **RQ 4.** Do countries with higher GDP invest higher percentage of their GDP in R&D as compared to countries with lower GDP?


## Conclusions

* **RQ 1.** 10 countries with the highest and lowest Research and Development expenditure (% of GDP) in last 10 years.
    * All developed and powerful economies in the top 10 list and war-torn countries/small states/developing African countries/ weak economies in the bottom 10 list.
    
* **RQ 2.** How has R&D expenditure (% of GDP) changed over the last 10 years for these countries?
    * Overall, both developed and developing countries have increased R&D expenditure to gain competitive advantage in science and technology.

* **RQ 3.** Is there a relationship between R&D expenditure and other Science and innovation indicators like researchers per million people, Scientific and technical journal articles, ICT goods and high technology exports, high-technology exports (current USD), etc.
    * The investment in R&D (as % of GDP) has strong positive correlation with some indicators like researchers per million but not with other scientific indicators like high technology exports or number of journal articles/publications. SO this indicator must be studied in conjunction with other human-centered factors.
    * Looking specifically at the case of high-technology exports as an example, we see how China ranks at the top with so many different factors affecting exports instead of just R&D expenditure.
    * There is also the need to consider innovation efficiency, unquantified research, and time gaps between grants and publications.
    * So higher R&D investment does not always guarantee proportional economic rewards.

* **RQ 4.** Do countries with higher GDP invest higher percentage of their GDP in R&D as compared to countries with lower GDP?
    * Yes, there is a positive relationship between the two indicators (~0.7) and all the countries in top 10 investor list have higher GDPs.


## License

#### User Guide Information (as stated on the World Bank site)

"Statistical tables that were previously available in the World Development Indicators print edition are now available online. Using an automated query process, these reference tables will be consistently updated based on the revisions to the World Development Indicators database. These reference tables were built using DataBank (http://databank.worldbank.org), an online web resource that provides simple and quick access to collections of time series data. It has advanced functions for selecting and displaying data, performing customized queries, downloading data, and creating charts and maps. DataBank reports can be easily edited, shared, and embedded as widgets on websites or blogs. For more information, see [here](http://databank.worldbank.org/help). Cell level metadata and values for years other than those specified can be highlighted by clicking the show metadata checkbox."

Citation: World Development Indicators, The World Bank

#### Data Access And Licensing

The World Bank Group makes data publicly available according to open data standards and licenses datasets under the Creative Commons Attribution 4.0 International license [CC-BY 4.0](https://datacatalog.worldbank.org/public-licenses#cc-by). Many datasets are available under other licenses. They are labeled accordingly, and when they are accessed by users, users agree to comply with all of the terms of the respective licenses, as explained [here](https://datacatalog.worldbank.org/public-licenses#cc-by).

## Course Wiki

This project is undertaken as the final project for the HCDS course at the UW:
https://wiki.communitydata.cc/Human_Centered_Data_Science_(Fall_2018)/Assignments

## Terms of Use

As mentioned on the World Bank site on [Terms of Use](http://www.worldbank.org/en/about/legal/terms-of-use-for-datasets) page:

Terms of Use for Datasets

The World Bank strives to enhance public access to and use of data that it collects and publishes. The data are organized in datasets listed in The World Bank Data Catalog (the “Datasets”). The Datasets are collections of data, managed by The World Bank and provided in a number of machine-readable formats. The World Bank provides you with access to the Datasets free of charge subject to the terms of this agreement (these “Dataset Terms”), and subject to the general Terms and Conditions for using the World Bank website, which are incorporated into these Dataset Terms.  Where these Dataset Terms conflict with the general Terms and Conditions, these Dataset Terms shall prevail. Use of data derived from the Datasets, which may appear in formats such as tables and charts, is also subject to these Dataset Terms.

Licenses

You are encouraged to use the Datasets to benefit yourself and others in creative ways. You may extract, download, and make copies of the data contained in the Datasets, and you may share that data with third parties according to these terms of use.

Unless specifically labeled otherwise, these Datasets are provided to you under a Creative Commons Attribution 4.0 International License (CC BY 4.0), with the additional terms below.  The basic terms may be accessed here.  When you download or use the Datasets, you are agreeing to comply with the terms of a CC BY 4.0 license, and also agreeing to the following mandatory and binding addition: 

Any and all disputes arising under this License that cannot be settled amicably shall be resolved in accordance with the following procedure:

  Pursuant to a notice of mediation communicated by reasonable means by either You or the Licensor to the other, the dispute shall be submitted to non-binding mediation conducted in accordance with rules designated by the Licensor in the copyright notice published with the Work, or if none then in accordance with those communicated in the notice of mediation. The language used in the mediation proceedings shall be English unless otherwise agreed.
 
  If any such dispute has not been settled within 45 days following the date on which the notice of mediation is provided, either You or the Licensor may, pursuant to a notice of arbitration communicated by reasonable means to the other, elect to have the dispute referred to and finally determined by arbitration. The arbitration shall be conducted in accordance with the rules designated by the Licensor in the copyright notice published with the Work, or if none then in accordance with the UNCITRAL Arbitration Rules as then in force. The arbitral tribunal shall consist of a sole arbitrator and the language of the proceedings shall be English unless otherwise agreed. The place of arbitration shall be where the Licensor has its headquarters. The arbitral proceedings shall be conducted remotely (e.g., via telephone conference or written submissions) whenever practicable
You agree to provide attribution to The World Bank and its data providers in the following format: The World Bank: Dataset name: Data source (if known). When sharing or facilitating access to the Datasets, you agree to include the same acknowledgment requirement in any sub-licenses of the data that you grant, and a requirement that any sub-licensees do the same. You may meet this requirement by providing the uniform resource locator (URL) of these terms of use.

You may use our application programming interfaces (“APIs”) to facilitate access to the Datasets, whether through a separate Web site or through another type of software application.

Exceptions for Some Third-Party Data

Some datasets and indicators are provided by third parties, and may not be redistributed or reused without the consent of the original data provider, or may be subject to terms and conditions that are different from those described above. Where applicable, these conditions are included in the dataset or indicator metadata.

Comments

We encourage you to share your suggestions and ideas for using or facilitating access to the Datasets with The World Bank.  If you have questions, seek to use Datasets on license terms other than the ones described above, or wish to make other comments, please contact us at +1 202 473 7824 or +1 800 590 1906, or by sending an email to data@worldbank.org.

No Endorsement

You may not publicly represent or imply that The World Bank is participating in, or has sponsored, approved or endorsed the manner or purpose of your use or reproduction of the Datasets. The World Bank may prosecute, to the fullest extent of the law, any use of Datasets in a manner that falsifies, misrepresents, disparages or fraudulently uses the Materials.

No Association

You may not use the name, any trade-mark, official mark, official emblem or logo of The World Bank, or any of its other means of promotion or publicity, without The World Bank's prior written consent nor in any event to represent or imply an association or affiliation with The World Bank.

No Warranties

The World Bank reserves the right at any time and from time to time to modify or discontinue, temporarily or permanently, this website, the Datasets, any means of accessing or utilizing the Datasets, or the API, at our sole discretion with or without prior notice to you.

The World Bank may at our sole discretion, under any circumstances, for any or no reason whatsoever and with or without prior notice to you, terminate your access to the Datasets, any means of accessing or utilizing the Datasets or the API.

THE WORLD BANK DISCLAIMS ALL WARRANTIES OF ANY KIND RELATED TO THE PROVISION OF THE DATASETS AND THE APIs. Please review the section of The World Bank Terms and Conditions under the heading Disclaimers, Releases and Limitations on Liability for a more complete statement regarding those subjects.

Exclusion of Liability

THE WORLD BANK SHALL NOT BE RESPONSIBLE OR LIABLE TO YOU FOR ANY LOSS OR DAMAGE OF ANY SORT INCURRED BY YOU IN CONNECTION WITH YOUR USE OF THE DATASETS. The World Bank also shall not be responsible or liable for the accuracy, usefulness or availability of any data in the Datasets. Please review the section of The World Bank Terms and Conditions under the heading Disclaimers, Releases and Limitations on Liability for a more complete statement regarding those subjects.

You acknowledge that these Dataset Terms constitute a non-exclusive agreement. The World Bank may develop products or services that compete with products or services that you offer without incurring any liability.

Other parties may have ownership interests in some of the data and information (“Materials”)  contained on the Site. The World Bank in no way represents or warrants that it owns or controls all rights in all Materials, and the World Bank will not be liable to you for any claims brought against you by third parties in connection with your use of any Materials.

Nothing herein shall constitute or be considered to be as an express or implied  limitation upon or waiver of the privileges and immunities of The World Bank, all of which are specifically reserved.

Other

Please review The World Bank Terms and Conditions prior to using the Datasets. These Dataset Terms incorporate the World Bank Terms and Conditions by reference. By using the Datasets or any presentations of data derived from them, or by using our APIs in connection with the Datasets, you consent to be bound The World Bank Terms and Conditions, including these Dataset Terms.

These Dataset Terms may be amended by The World Bank from time to at our sole discretion. Please periodically review the controlling version of these Dataset Terms. By continuing to use the Datasets subsequent to The World Bank making available an amended version of these Dataset Terms, you acknowledge, agree and consent to such amendment.


