---
layout: page
title: Delancey's Elephant & Castle
subtitle: '979 new homes, not enough social rented. Little room for current shopkeepers'
sharing: true
published: true
---
![]({{site.baseurl}}/img/delanceyaerial.png)

Despite attracting over [a thousand formal objections](https://planning.southwark.gov.uk/online-applications/applicationDetails.do?activeTab=makeComment&keyVal=_STHWR_DCAPR_9569810) and after [failing to get approval](https://www.bbc.co.uk/news/uk-england-london-42719607) from Southwark's planning committee on 16 Jan 2018, developer Delancey's [application](http://planbuild.southwark.gov.uk/documents/?casereference=16/AP/4458&system=DC){:target="_blank"} for the redevelopment of the [Elephant & Castle shopping centre](http://35percent.org/shopping-centre/){:target="_blank"}, was [narrowly approved](http://35percent.org/2018-07-09-delancey/) on 3 July 2018, after a total of three deferments.

## Affordable housing
Delancey has been granted permission to build 979 Build to Rent homes totalling 106,471sqm of residential floorspace and while 35% will be 'affordable' only 9,141sqm (8.6% - 116 homes) will be social rent. 

None of this is in line with the [Elephant's current affordable housing policy](http://www.southwark.gov.uk/assets/attach/1817/1.0.5%20Elephant%20%26%20Castle%20SPD%20OAPF.pdf), which requires half (17.5%) of the minimum 35% affordable housing to be social rented. This should give us nearly 170 social rented units. Instead we are getting only 116 social rented units with 53 'London Living Rent equivalent' units (£205 - £308pw) and 161 affordable rent at up to 80% market rent, for household incomes up to £90,000pa. Measured by floorspace the social rent element is only 8.6% of the total residential floorspace.

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js">
</script>
<script src="http://code.highcharts.com/highcharts.js">
</script>
<script src="http://code.highcharts.com/modules/exporting.js">
</script>
<script src="https://code.highcharts.com/modules/export-data.js">
</script>

<div id="container" style="min-width: 310px; height: 400px; margin: 0 auto">
</div>

<script type="text/javascript">
var colors = Highcharts.getOptions().colors,
  categories = [
    'Private: 65%',
    'Social Rent: 17.5%',
    'Intermediate: 17.5%'
  ],
  data = [
    {
      y: 65.0,
      color: colors[2],
      drilldown: {
        name: 'Market Rent',
        categories: [
         'Market Rent'
        ],
        data: [
          65.0
        ]
      }
    },
    {
      y: 17.5,
      color: colors[1],
      drilldown: {
        name: 'Social Rent',
        categories: [
          'Social Rent',
          'Intermediate Rent'
        ],
        data: [
          8.6,
          0.0
        ]
      }
    },
    {
      y: 17.5,
      color: colors[0],
      drilldown: {
        name: 'Intermediate Housing',
        categories: [
              'Intermediate Rent'
        ],
        data: [
          26.4
        ]
      }
    }
  ],
  browserData = [],
  versionsData = [],
  i,
  j,
  dataLen = data.length,
  drillDataLen,
  brightness;


// Build the data arrays
for (i = 0; i < dataLen; i += 1) {

  // add browser data
  browserData.push({
    name: categories[i],
    y: data[i].y,
    color: data[i].color
  });

  // add version data
  drillDataLen = data[i].drilldown.data.length;
  for (j = 0; j < drillDataLen; j += 1) {
    brightness = 0.2 - (j / drillDataLen) / 5;
    versionsData.push({
      name: data[i].drilldown.categories[j],
      y: data[i].drilldown.data[j],
      color: Highcharts.Color(data[i].color).brighten(brightness).get()
    });
  }
}

// Create the chart
Highcharts.chart('container', {
  chart: {
    type: 'pie'
  },
  title: {
    text: 'Approved Tenure Mix'
  },
  subtitle: {
    text: 'Source: <a href="http://planbuild.southwark.gov.uk/documents/?casereference=16/AP/4458&system=DC" target="_blank">Southwark Council planning ref:16/AP/4458</a>'
  },
  plotOptions: {
    pie: {
      shadow: false,
      center: ['50%', '50%']
    }
  },
  tooltip: {
    valueSuffix: '%'
  },
  series: [{
    name: 'Policy Requirement',
    data: browserData,
    size: '60%',
    dataLabels: {
      formatter: function () {
        return this.y > 5 ? this.point.name : null;
      },
      color: '#ffffff',
      distance: -30
    }
  }, {
    name: 'Approved percentage',
    data: versionsData,
    size: '80%',
    innerSize: '60%',
    dataLabels: {
      formatter: function () {
        // display only if larger than 1
        return this.y > 1 ? '<b>' + this.point.name + ':</b> ' +
          this.y + '%' : null;
      }
    },
    id: 'versions'
  }],
  responsive: {
    rules: [{
      condition: {
        maxWidth: 400
      },
      chartOptions: {
        series: [{
          id: 'versions',
          dataLabels: {
            enabled: false
          }
        }]
      }
    }]
  }
});
        
</script>

Nor does the affordable housing offer meet the required amounts in the [new, 'emerging' policy](https://www.southwark.gov.uk/planning-and-building-control/planning-policy-and-transport-policy/development-plan/local-plan?chapter=4) Southwark is trying to sneak through the backdoor, to help the likes of Delancey reduce their affordable housing obligations.  Southwark has previously vehemently [argued against including affordable rent in local housing policy](http://35percent.org/redefining-social-rent/). Delancey's offer will do nothing to offset the poor balance of social housing provision in the regenerated Elephant & Castle's new developments.

As is usual, Delancey has submitted a viability assessment claiming that its affordable housing offer is the most than can be viably provided, but this falls way short of what Southwark's planning policy requires, as is also usual. Since its initial offer of 33 homes at 'social rent equivalent', Delancey has upped the number, first to 74 and then to 116, but this is still short of the amount needed for policy compliance. 

Delancey claims to have a £11.25m social housing grant from the Greater London Authority (GLA), but if this is so, it has found its way straight to Delancey's bottom line, increasing its profit by the same amount.  We can see this by comparing two development appraisals of the scheme.  [The first](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!eW5y4yYs725p%2bJMli9Cf8g%3d%3d!%7d%7d%7d), dated 13 June 2018, is for a scheme with 116 social rented units, but without grant funding, and has a profit of £137.1m.  [The second](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!rcfVT8LTb%2bOXBtPlyVeyXg%3d%3d!%7d%7d%7d), dated 22 June 2018, is also for a scheme with 116 social rented units, but includes the £11.25m GLA grant, and, by a miracle of development finance, a profit of £148.4m. [Delancey have responded](https://twitter.com/ShapingElephant/status/1012006789997580294?s=19the) to justified [cries of 'subsidise homes, not profit'](https://twitter.com/occupyelephant?lang=en) pretty much confirming that this is what has happened, but referring to the difference in the profit levels as a 'viability gap' and pleading that it 'maintains' the profit, not 'enhances' it.  Most people will struggle to see the difference and would think the money better spent on the social housing Delancey claims it cannot afford to build.

![](/img/delanceyfvaprofit.png)

Southwark argues that it has secured a 'viability review' mechanism in the [legal agreement](https://docdro.id/wIuSC8m) ensuring that any surplus above Delancey's anticipated profit will go towards providing additional affordable housing. But the agreement only makes provision for half of any surplus to go towards this, the other half is to be retained by Delancey.

Further doubt about Delancey's viability assessment is raised by the Council's independent advisors [(GVA)](http://www.gva.co.uk) who produced a [report](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!PHUQPPiesgvQWEZYj1nx%2fw%3d%3d!%7d%7d%7d)  explaining that Delancey had listed a £14.5m CPO liability as a cost to the scheme. GVA says Delancey provided this £14.5m figure without providing sufficient information to justify it.

![](/img/sccpo.png)

While Delancey has reached agreement with the bingo hall and the handful of traders who had leases extending beyond 2019, as well as the freehold owners of the pub.  The two terraced properties adjacent to the Coronet [remain in the hands of the shopowners](/img/30and32NewKentRoad.pdf). Whether any settlements collectively amount to £14.5m or whether a CPO will be needed still remains to be seen.

![](/img/davishcropped.png)

In addition, Delancey's viability assessment claimed a £92m acquisition cost for the shopping centre site. This is £12m more than it [actually paid for the site](http://crappistmartin.github.io/images/LRDeeds_ShoppingCentre.pdf) and is yet another way of making the scheme look less profitable than it actually is.

![](/img/fvaeastsiteacq.png)
 
## Offshore Elephant
Delancey's 'Build-to-Rent' homes will be privately managed by its subsidiary __Get Living London__. Despite [managing over £1bn worth of PRS homes](http://www.propertyweek.com/news/get-living-to-double-assets-to-%C2%A32bn/5088136.article) __Get Living London__ has [never paid a penny of corporation tax](https://beta.companieshouse.gov.uk/company/07793925/filing-history). This is because its parent companies are [Qatari Diar](http://www.cityam.com/238088/elephant-castle-scheme-and-east-village-site-merged-to-create-14bn-private-rented-sector-venture){:target="_blank"} and Delancey's [tax-avoiding](http://crappistmartin.github.io/images/PrivateEyeNo1311.pdf){:target="_blank"} offshore investment fund DV4 registered in the British Virgin Islands. The Elephant and Castle shopping centre is currently owned by one of the fund's shell companies [registered in the BVI](http://crappistmartin.github.io/images/LRDeeds_ShoppingCentre.pdf){:target="_blank"} and whose directors are [registered](https://beta.companieshouse.gov.uk/company/04434716/officers){:target="_blank"} in Bermuda and Kuwait. We have shown before how Delancey uses a [complex network of offshore companies](http://35percent.org/2014-05-05-manx-connections-the-off-shore-home-of-the-elephants-developers/) to avoid paying tax.

![Delancey's Elephant & Castle holdings registered in the BVI](/img/shoppingcentrelr.png)

## What about existing retailers?
As expected the shopping centre is to be demolished and just 10% of the redeveloped site will be 'affordable retail' with sub-market rents for the first 15 years. Delancey's [planning statement](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!LnbCaTCiMmUoN4H%2fUA2yyg%3d%3d!%7d%7d%7d){:target="_blank"} contends that _'it is recognised that some existing retailers in the area are benefitting from disproportionately low levels of rent...'_ and concludes that _'it may not be financially viable for them to survive in the area in the longer term'_. 

![](http://35percent.org/img/traderscomp.jpeg)

Delancey's neighbouring development [Elephant One](/tribeca-square) was supposed to provide affordable retail space for some of the displaced traders. In 2015, we [revealed](http://35percent.org/2015-07-12-shopping-centre-and-lcc-redevelopment-proposals/#delancey---a-morality-tale){:target="_blank"} how Delancey had successfully lobbied the Council to change the conditions of its planning permission to switch some of these units for a Sainsbury's.

Ater their [failure](https://www.bbc.co.uk/news/uk-england-london-42719607) to get their plans approved in Jan 2018, Delancey [agreed to provide](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!0iVzasdHCgb1eVmQCrssOg%3d%3d!%7d%7d%7d) a temporary retail ['box park'](/boxpark) at discounted rents, using shipping containers at neighbouring Castle Square, which is on council-owned land but [leased to Delancy on a peppercorn rent](http://35percent.org/2016-06-26-restricted-access-elephant-park/#elephant-parks) and a share of the revenue from the Square's future street market. 

![](http://35percent.org/img/tempboxpark.png)

The Castle Square facility would last for 5 years, or until the Elephant & Castle Shopping Centre development has been completed.

The facility is small consolation for the traders, who have [objected](https://planning.southwark.gov.uk/online-applications/applicationDetails.do?activeTab=neighbourComments&keyVal=_STHWR_DCAPR_9578882) that the proposed building is too small and would have trading restrictions that would make it an impractical premises for many of the displaced businesses. [Delancey's  proposals](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!hAV0cqN%2bsOq%2febuFpH0spQ%3d%3d!%7d%7d%7d) mention 33 independent traders, while the trader's own estimate is that there is a need to provide for nearly 100 traders. While a late concession set the rent levels at [£18-£24psf](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!f8wi7RxxFnE3Bd3xh6Hkzg%3d%3d!%7d%7d%7d), other issues remain, including the level of service charges, the security of tenacy arrangements and selection criteria. Castle Square and the other potential relocation site options (including Perronet House, Elephant One, and Elephant Park) provide about [two-thirds of the space traders need](https://docdro.id/e2lWS4h).

In April 2019, it was [reported](https://www.londonnewsonline.co.uk/traders-fume-at-being-ousted-from-the-elephant-castle-shopping-centre/) that only 36 of the 79 traders in the shopping centre and market have been offered temporary relocation space and that the market traders in the outskirts of the centre had been largely ignored. We subsequently [found](http://35percent.org/2019-03-30-no-room-for-traders-in-the-new-elephant/#no-room-on-the-park) that Lendlease has been refusing to allocate traders to the designated affordable retail space in its neighbouring 'Elephant Park' development.

In 2005, Southwark was [slated by Lord Ouseley after an independent review](http://35percent.org/2015-11-04-southwark-resolves-to-use-cpo-powers-for-shopping-centre-retailers/){:target="_blank"} found that its regeneration policies failed retailers and traders from BME communities. These failings clearly continue.

![](http://www.social-life.co/media/cache/7c/d8/7cd88351c83035bea1af1a55ffe6d81a.jpg)

Delancey's application is just another step down the gentrification road. The shopkeepers and small traders, many from ethnic minority backgrounds, who have worked hard to become an integral part of the community, are deemed to be _'not financially viable ...to survive'_. Southwark Council and the Mayor should be telling Delancey how unacceptable this application is. They should be promoting London's diverse economy - not letting developers like Delancey kill it. 

## History
The Elephant & Castle shopping centre used to be owned by Godfrey Bradman, the property tycoon who redeveloped the City of London's [Broadgate estate](http://en.wikipedia.org/wiki/Broadgate){:target="_blank"} in the 1980s.

Bradman was originally selected as the council's development partner for the E&C regeneration back in April 2000, but his [masterplan](http://embed.verite.co/timeline/?source=0Aprl6XcACewydEhRaWFOLVBfUjBSVW1HUGVZNEhGeFE&font=Bevan-PotanoSans&maptype=toner&lang=en&hash_bookmark=true&start_zoom_adjust=2&height=650#6){:target="_blank"} came to an abrupt end when Southwark [terminated negotiations](http://embed.verite.co/timeline/?source=0Aprl6XcACewydEhRaWFOLVBfUjBSVW1HUGVZNEhGeFE&font=Bevan-PotanoSans&maptype=toner&lang=en&hash_bookmark=true&start_zoom_adjust=2&height=650#7){:target="_blank"} in April 2002.

The shopping centre was then [sold](http://www.standard.co.uk/business/markets/property-southwark-gets-a-new-lease-of-life-8841328.html){:target="_blank"} to a joint-venture between Kuwaiti real-estate group [__Salhia__](http://www.salhia.com){:target="_blank"} and West Midlands-based regeneration developer [__St Modwen__](http://stmodwen.co.uk){:target="_blank"} for £29m in 2004.

Having lost out to Lendlease in its 2007 bid to be the council's regeneration partner for the Elephant, including the Heygate estate, St Modwen put forward its proposals to the council for the redevelopment of the shopping centre. But it was knocked back due to the large number of residential units it wanted to build on the site; St Modwen [said](http://www.london-se1.co.uk/news/view/5831){:target="_blank"} it needed to include 1000 residential units in the development to make it viable, but the council said it would [refuse](http://crappistmartin.github.io/images/Estates_Gazette_18March2014.pdf){:target="_blank"} to consider more than 500.
 
As a result of the stalemate, St Modwen [sold](http://crappistmartin.github.io/images/LRDeeds_ShoppingCentre.pdf){:target="_blank"} the shopping centre in 2014 for £80m to __Delancey DV4__, a developer funded by George Soros, managed by [Tory donor](http://www.independent.co.uk/news/uk/politics/party-funding-tory-coffers-benefit-from-fear-of-labour-mansion-tax-9716614.html){:target="_blank"} Jamie Ritblatt, registered in the British Virgin Islands and which has been [accused](http://crappistmartin.github.io/images/PrivateEyeNo1311.pdf){:target="_blank"} of _'aggressive tax avoidance'_. Jamie is son of Sir John Ritblat, property tycoon who owns __British Land__ and is a long-standing Tory donor. __British Land__ has been selected as the Council's development partner for its massive [46-acre Canada Water regeneration scheme](http://35percent.org/canada-water/#british-land-masterplan-site). 

![](http://35percent.org/img/jamieandjohnritblat.jpg)
*Jamie Ritblat(left) and Sir John Ritblat(right)*

Delancey, which is also developing neighbouring site ['Elephant One'](http://crappistmartin.github.io/tribeca-square){:target="_blank"}, [employed](http://crappistmartin.github.io/images/delanceyinvite.pdf){:target="_blank"} former deputy Southwark council leader [Kim Humphries](http://www.linkedin.com/pub/kim-humphreys/5/312/a34){:target="_blank"} to advise on its development and lead its consultation plans. Kim is now ['Carvil Ventures Ltd'](http://carvil-ventures.co.uk/){:target="_blank"} - an independent corporate finance and real-estate consultancy, which is advising Delancey. Kim [made his name](https://youtu.be/E9-cfAdGiFA?t=6m44s){:target="_blank"} in the [Heygate clearances](http://35percent.org/2013-06-08-the-heygate-diaspora/){:target="_blank"} and is not the first Council member to disappear through Southwark's [revolving doors](/revolving-doors){:target="_blank"}. 

![Kim Humphries](/img/carvilkimcollage.jpg) 
*Former deputy Council leader Kim Humphries - now working for Delancey*

## Coronet 
Delancey dismissed the [campaign](http://coronettheatre.co.uk/home/save-the-coronet/){:target="_blank"} to save [The Coronet](http://www.theatrestrust.org.uk/resources/theatres/show/3344-coronet-london){:target="_blank"}. The Coronet takes up a sizeable part of the shopping centre site. A music and event venue, it has also been a cinema and music hall [dating back to 1872](http://www.london-se1.co.uk/news/view/7701){:target="_blank"} and is a popular local institution. Attempts have been made to have it listed on the basis of its Art Deco interior and exterior, which currently remains [hidden](http://crappistmartin.github.io/images/SNcoronet.pdf){:target="_blank"} behind its blue corrugated facade, but Delancey's scheme will see the venue bulldozed. The [Theatres Trust](http://www.theatrestrust.org.uk/){:target="_blank"} submitted a [strong objection](planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!mXJGLVs8phU8UfW%2b%2fP0kZA%3d%3d!%7d%7d%7d){:target="_blank"} to Delancey's planning application. 

![](http://crappistmartin.github.io/images/coronet_cinema.jpg)

## Bingo
Palace Bingo hall on the first floor of the shopping centre is an important local community facilty, accommodating around 500 pensioners daily. Southwark's [planning committee report](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!HvOs1eG7BYgl0hYZ8SIm5w%3d%3d!%7d%7d%7d) acknowledges that the bingo hall is _"clearly a popular and well-used facility"_ and _"that a high proportion of elderly people and people from Black, Asian and Minority
Ethnic (BAME) backgrounds use the facility, and its loss could result in adverse equality implications."_ It then goes on to explain that this is 'mitigated' by Delancey's offer to give 'first right of refusal' to a bingo operator for use of some of the new leisure space in its scheme (para 125).  

![](/img/palacebingo.jpg)

In Palace Bingo's [response to this](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!mlQECLDoZucrky0D%2fJLzhw%3d%3d!%7d%7d%7d) it said: _"At the time of publishing the report and your Cabinet meeting there had been no dialogue[with Delancey], and subsequent discussions have not been meaningful or substantive thus far."_ In March 2019 the Bingo Hall closed and the operator has no plans to return to the redeveloped centre.

## Transport
Transport for London's [initial response to the scheme](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!eFbtnvDjhOiqL4IpxHg%2f%2fw%3d%3d!%7d%7d%7d){:target="_blank"} outlined a number of significant transport issues that needed to be resolved. One of these was the access route for service vehicles to the new shopping centre, which was originally going to be provided by an underground tunnel from Delancey's neighbouring [Elephant One](/tribeca-square) (formerly Tribeca Square) development. Indeed, Delancey's [viability assessment](http://crappistmartin.github.io/images/Delancey_Tribeca_ViabilityAssessment.pdf) for Elephant One argued that the ramp for the underground tunnel would cost £12.5m and the development could therefore not viably provide ANY affordable housing. The council accepted the argument and even [signed over land](/img/DelanceyEadon_MarketSquare_Agreement.pdf) to Delancey's shell company (Eadon Ltd), in order to build the underground access tunnel. However, Delancey's planning application now says that it wants to use a different, direct access route off New Kent Road instead. TFL says that this will cause congestion for buses and affect safe passage across the new pedestrian routes.

![](/img/shoppingcentreaccess.png)

TFL also raised the issue of the mainline train station. This sits at the centre of the redevelopment and will have to cope with a huge capacity increase, but will have no improvements made to it whatsoever. Another major question surrounds the proposed Bakerloo line extension, announced after the Delancey's development plans were drawn up, and how this will impact on the Elephant's transport links.  The [original masterplan](https://www.scribd.com/doc/198503633/EandC-RegenMk1SLRplans){:target="_blank"} envisaged an 'integrated transport interchange' linking the mainline train station with the Northern and Bakerloo lines, and which was central to the entire masterplan.

![](/img/transporthub.png)
*Transport interchange envisaged by [original masterplan](https://www.scribd.com/doc/198503633/EandC-RegenMk1SLRplans){:target="_blank"}*

Southwark's own [__Design Review Panel__](https://www.southwark.gov.uk/planning-and-building-control/design-and-conservation/design-review-panel) criticised Delancey's scheme heavily, in particular with relation to the transport interchange. In their [report](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!Lne%2f9qVjTGbWyUdbJYdnsw%3d%3d!%7d%7d%7d) to the Council's planning committee they said that the _"significant size and scale of the proposed UAL and the shopping centre buildings adjacent to the viaduct which block off access to the station from the north or south along the viaduct."_

It goes on to raise _"significant concerns"_ about the building infront of the railway station _"Firstly, the scale of the building and how it affects the generosity of Elephant Court which is severely restricted as a consequence and does not have the proportions of a civic square which a scheme of this scale will require. Secondly, ‘Elephant Court will be an importance entrance point for the railway station at the Elephant and Castle from the west. This includes the interchange from the new underground station at the Elephant and Castle peninsula. The Panel felt the current proposal does not demonstrate how this important transport interchange will be facilitated by the scheme and remained concerned that the new building will impede access to the railway station._" 

The panel raises significant concerns about the new Northern line entrance, which they felt _"lacked visual presence on the street and is currently proposed as a simple single-storey shopfront – no different to a retail unit."_

It also criticises Delancey's public realm proposals; _"In respect of the public realm, the Panel felt the current proposals lacked generosity. They noted that other significant schemes provided appropriate civic spaces and public realm on their sites and felt that the current proposal did not strike the right balance between pubic realm and built form to mitigate against the enormous scale of the proposal."_

## Public Realm
 [Land Registry Records](http://35percent.org/lrdeeds/shoppingcentreCouncilFreeholdLand.pdf) show that the Council is handing over a considerable amount of public realm to Delancey for its disastrous and inqequitable redevelopment of the E&C shopping centre.

The [S106 legal agreement](/img/ShoppingCentreS106.pdf) shows that the entire public realm in Delancey's redeveloped Elephant & Castle will be privately managed and the Delancey reserves the right to 'eject' anyone it considers an 'annoyance':

![](/img/s106annoyance.png)
*Extract from the [S106 legal agreement](/img/ShoppingCentreS106.pdf) showing public realm clause*

![](/img/scpublicrealm.jpg)
*Extract from the [S106 legal agreement](/img/ShoppingCentreS106.pdf) showing new public realm*


## Renewable Energy
The original regeneration plans proposed a [Multi-Utility Services Co.](http://www.london-se1.co.uk/news/view/2270) (MUSCo) renewable energy plant, which was [supposed](https://www.southwark.gov.uk/assets/attach/1814/Elephant_and_Castle_Regeneration_Agreement_Appendix_6.pdf) to provide _"the generation of renewable energy"_ in a _"sustainable network of heat, water and telecoms"_ for all new developments at the Elephant. The MUSCo was going to generate 100% renewable energy from a biomass energy centre making the Elephant & Castle regeneration a 'zero carbon' development with 'carbon positive' homes.

![](http://crappistmartin.github.io/images/MuscoNetwork.png)

The MUSCo was also [going to supply](http://moderngov.southwark.gov.uk/mgConvert2PDF.aspx?ID=16241) the new Aylesbury estate development and the existing Salisbury and Newington housing estates, making it the [largest biomass-fuelled district heating network](/images/muscoarea.png) in London. The plans were so cutting edge that they were [praised](http://news.bbc.co.uk/1/hi/england/london/8056859.stm) by Bill Clinton and [included](http://www.london-se1.co.uk/news/view/6032) in the [C40 Climate Positive Development Programme](https://en.wikipedia.org/wiki/Climate_Positive_Development_Program)._ However, the plans have been dropped because the costs were too high. The scheme had become a _'fairy tale fantasy'_ [according](http://www.london-se1.co.uk/news/view/5052) to the Council's own cabinet member for regeneration. Now, instead the Elephant & Castle shopping centre/UAL development will [provide just 35 solar panels](http://planbuild.southwark.gov.uk/documents/?GetDocument=%7b%7b%7b!ocfCH8IZNlNKf8lwnyuxDQ%3d%3d!%7d%7d%7d) representing a measly 1% renewable energy. This falls well short, not just of the Council's zero carbon policy for the Elephant & Castle but also its borough-wide policy requiring a minimum 20% renewable energy for all new major schemes. 

![](/img/scpv.png)

## Legal Challenge
We have helped to [crowdfund a legal challenge](https://www.crowdjustice.com/case/save-the-elephants-diverse-com-appeal/) to Delancey's plans, which seeks to quash the planning consent and send these inequitable plans back to the drawing board until a scheme comes forward that provides new homes and shops that are truly affordable for local people.


<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:site" content="@35percent_EAN">
<meta name="twitter:title" content="Delancey's Elephant and Castle">
<meta name="twitter:description" content="1000 new homes but only 8.6% social rent - only 10% of new retail earmarked for current traders.">
<meta name="twitter:image" content="http://35percent.org/img/shoppingcentrecomp.png">
