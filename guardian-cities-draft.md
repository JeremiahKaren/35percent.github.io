---
layout: post
title: Why we're challenging the Elephant & Castle redevelopment plans in court
author: Jerry F
published: true
---


We are a coalition of local people and groups fighting for fairer regeneration at the Elephant and Castle and we are taking our local council to court to try to overturn a planning permission awarded to property developer Delancey to demolish and redevelope the Elephant shoping centre. We are doing this because we were promied a regeneration that was supposed to deliver jobs and homes for local people, but is doing the exact opposite.

Twenty years ago, almost to the day, Fred Manson, Southwark Council's Director of Regeneration laid out the aims of the Labour council's new regeneration strategy in the Estates Gazette: _"We need to have a wider range of people living in the borough"_ because _"social housing generates people on low incomes coming in and that generates poor school performances, middle-class people stay away."_ As the Gazette reported it, this was _'part of a deliberate process of gentrification that will result in social housing being replaced by owner occupied dwellings and developers being given free reign to build luxury flats'_[^1].


Since Mr Manson's anti-council housing manifesto in 1999, Southwark has lost more than 13,000 council homes and the proportion of council housing in the borough has fallen from 60% to 28% of housing stock.  This is mainly the consequence of [Right to Buy](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/759390/LT_685.xlsx) and [void sales](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/561232/LT_648.xlsx). 

But estate regeneration is also playing its part. The Gazette article mentions three estates south of Tower Bridge earmarked for demolition. At [least eight others](http://35percent.org/the-southwark-clearances) can be added, totalling 7,639 council homes when originally built.  The developments replacing these will provide over 11,000 new homes, but only 3,200 of them will be social rented.  

Other major schemes are worse.  A sample of 25 developments, including some estate regenerations, gives [an average social rent component of under 4%](http://35percent.org/major-schemes) out of about twelve thosand homes- well below the Council's [policy requirement of 25%](LINKTONSP) and while Southwark does now have an council house building programme, it is [still knocking down and selling off council homes faster than it is building them](http://35percent.org/2018-11-12-11000-council-homes-manifesto-pledge/).

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js">
</script>
<script src="http://code.highcharts.com/highcharts.js">
</script>
<script src="http://code.highcharts.com/modules/exporting.js">
</script>

<div id="container1" style="min-width: 310px; height: 400px; margin: 0 auto">
</div>

<script type="text/javascript">

        $('#container1').highcharts({
            title: {
                text: "Southwark's Council Homes",
                x: -20 //center
            },
            subtitle: {
                text: 'Source: https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/674346/LT_116.xlsx',
                x: -20
            },
            xAxis: {
                categories: ['1999', '2000', '2001', '2002', '2003', '2004', '2005', '2006', '2007', '2008', '2009', '2010', '2011', '2012', '2013', '2014', '2015', '2016', '2017']
            },
            yAxis: {
                title: {
                    text: 'Council-owned stock'
                },
                plotLines: [{
                    value: 0,
                    width: 1,
                    color: '#808080'
                }]
            },
            tooltip: {
                valueSuffix: ' Council homes'
            },
            legend: {
                layout: 'vertical',
                align: 'right',
                verticalAlign: 'middle',
                borderWidth: 0
            },
            series: [{
                name: 'Southwark',
                data: [51706, 50903, 49875, 48052, 46887, 45346, 43885, 42275, 41873, 41287, 40618, 40120, 39845, 39781, 38578, 39029, 38687, 38522, 38553]
            }]
        });

</script>

The [Elephant and Castle shopping centre redevelopment](http://35percent.org/shopping-centre) is no exception to this trend.  A stone's throw from the demolished Heygate estate, only 116 of nearly a thousand new homes will be offered as social rent (8.6% by floorspace), all to built nearly tens years hence.  Shopping centrre owner and developer Delancey (link) said that this was as much as it could afford to build, but we now know that with Mayor’s funding they could give us another 42 homes - still a modest amount, but enough to reach Southwark's local plan requirement. 

<div id="container2" style="min-width: 310px; height: 400px; margin: 0 auto"></div>

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
Highcharts.chart('container2', {
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

There is also doubt about how well any of the social housing has been secured.  Leaving aside the fact it won't be built for ten years, a long time by any measure, Delancey has the option of passing the obligation to build the homes back to Southwark to fufil, along with land and 'sufficient funds' to do so.  We fear the development's legal agreement fails to properly guarantee this will happen. We also believe the legal agreement fails to provide an effective 'viability review mechanism' - a way to get greater affordable and social rent housing, should the develpment prove more profitable than expected.

Housing is one part of the development.  There will also be about the same amount of retail space as there is in the present shopping centre, but catering for the more well-healed customer other social-rent free developments are now drawing to the Elephant.  The shopping centre itself will be demolished, which will destroy not just the traders that have made the Elephant their home, including many ethnic businesses, but one of two major social hubs for the Latin American community in London (the other in Seven Sistes is under similiar threat - link).  The centre also has a large thriving bingo hall and bowling alley that will fall to the demolition ball (link). 

Concerted campaigning has gained some space for these traders in this new development and others, as well as a temporary relocation facility, but there is not enough space for every trader who wants it (link).  Latin Elephant (link), a local charity and advocate for all ethnic traders in the area reckons there are nearly a hundred independent traders in the area and, given the practicalities only a minority of traders are likely to benefit.

Delancey's anticipated profit from all of this is £137m, according to the scheme's viability assessment (link).  Delancey is Britain's largest private development company and, not unusually is based off-shore, althoough it insists this is not for tax-reasons. 

## Homelessness by design

Delancey and Southwark argue that other elements of the scheme - a new Northern Line tube entrance and a campus for the London College of Communication provide positives - outweigh any negatives.  This is entirely in keeping with the regeneration rationale, as articulated by Mr Manson back in 1999, so successfully implemented by Southwark since and making a healthy contribution to London's disastrous housing situation - thousands of new homes that many, not just of the poorest, can afford to neither rent nor buy; housing costs for those poorest [the 'worst in Europe'](https://www.theguardian.com/society/2018/mar/21/uk-europe-housing-cost-rise-lowest-earners-report) and a [record number of rough sleepers](https://www.theguardian.com/society/2018/oct/31/record-number-of-people-are-sleeping-rough-in-london)

Local campaigners, with the support of thier local councillors have fought hard over the past two years to squeeze housing concessions and a better deal for shopping centre traders.  Southwark Council, on the other hand has been content to take whatever it was offered, in pursuit of its wretched gentrification agenda.  Fourty two extra social rented homes may not be many, but it is what Southwark's own local plan requires, the London Mayor has the money to pay for it and we are determined that it should be built.

That is why We are challenging Delancey’s planning permission through the Planning Court.  We want the permission quashed and then we want a development scheme at the Elephant and Castle that can have a new that provides homes and shops that are truly affordable for local people.  




![](http://35percent.org/img/traderscomp.jpeg)



----------------------------------------------------------------------------------------------------

'He went on to point out that 60% of housing in Southwark is social housing and that the Council's new policy was aimed at reversing some of the problems caused by past social engineering[^1].

Delancey claims it is building a 'new town centre' for Elephant and Castle but there will be nearly six times more residential than retail floorspace in the new scheme (106,471sqm residential vs 18,234sqm retail). [^2].

Only 10% of the new retail space will be provided at affordable rates to accommodate existing independent traders, who will pay a discounted rent of 40 per cent market rate for a five year period and 75 per cent for the subsequent ten. This concession was only won from Delancey after a bitter campaign struggle. Delancey was originally offering only x%?? affordable retail and only discounted for the first 5 years. 


In any event it is still not enough - the Elephant's diverse community of independent traders make the place what it is and there will be no place for 90% of them if Delancey's plan is allowed to proceed.


![](http://35percent.org/img/delanceyshoppingcentrecgi.jpg)

__Footnotes:__

[^1]: Estates Gazzette article [published 13 March 1999](http://heygate.github.io/img/EstatesGazette.pdf)

[^2]: See paragraph 19 of the Officers report [insert link].
