---
layout: post
title: "Why we're challenging the Elephant & Castle redevelopment plans in court"
author: Jerry F 
---
Twenty years ago today Fred Manson, Southwark's Director of Regeneration laid out the Council's new regeneration strategy: _"We need to have a wider range of people living in the borough"_ because _"Social housing generates people on low incomes coming in and that generates poor school performances, middle-class people stay away."_ He went on to point out that 60% of housing in Southwark is social housing and that the Council's new policy was aimed at reversing some of the problems caused by past social engineering[^1].

Twenty years on and Southwark's reverse social engineering has been a resounding success. More than 13,000 Council homes have been [lost through Right to Buy, void sales and estate regenerations](http://35percent.org/the-southwark-clearances) while tens of thousands of new homes have been built [with an average social rent component of under 4%](http://35percent.org/major-schemes) - well below the Council's [policy requirement of 25%](LINKTONSP). While Southwark does now have an ambitious council house building scheme, it is [still knocking down and selling off council homes faster than it is building them](http://35percent.org/2018-11-12-11000-council-homes-manifesto-pledge/).

<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js">
</script>
<script src="http://code.highcharts.com/highcharts.js">
</script>
<script src="http://code.highcharts.com/modules/exporting.js">
</script>

<div id="container" style="min-width: 310px; height: 400px; margin: 0 auto">
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
                categories: ['1994', '1995', '1996', '1997', '1998', '1999',
                    '2000', '2001', '2002', '2003', '2004', '2005', '2006', '2007', '2008', '2009', '2010', '2011', '2012', '2013', '2014', '2015', '2016', '2017']
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
                data: [55803, 55162, 54439, 53363, 52448, 51706, 50903, 49875, 48052, 46887, 45346, 43885, 42275, 41873, 41287, 40618, 40120, 39845, 39781, 38578, 39029, 38687, 38522, 38553]
            }]
        });

</script>

The Elephant and Castle scheme is no exception to this trend with only 116 of nearly a thousand new homes offered as social rent (8.6% by floorspace).  

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

It has since emerged that developer Delancey was not upfront with councillors about the viable number of social rented homes in the scheme, its grant funding application or how they would be delivered. We have decided to take the matter to court and seek to have the planning consent quashed on this basis. (Maybe say more here about the grounds - i.e. the fact that Delancey promised 'sufficient funds' to construct the 116 units but the S106 fails to secure this; the fact that the S106's viability review promised to councillors is restricted from providing any further uplift in SR units).

The planning decision was controversial from the outset; it attracted over [a thousand formal objections](https://planning.southwark.gov.uk/online-applications/applicationDetails.do?activeTab=makeComment&keyVal=_STHWR_DCAPR_9569810) and after [failing to get approval](https://www.bbc.co.uk/news/uk-england-london-42719607) from Southwark's planning committee on 16 Jan 2018, developer Delancey's [application](http://planbuild.southwark.gov.uk/documents/?casereference=16/AP/4458&system=DC){:target="_blank"} for the redevelopment of the [Elephant & Castle shopping centre](http://35percent.org/shopping-centre/){:target="_blank"}, was [narrowly approved](http://35percent.org/2018-07-09-delancey/) by just one vote on 3 July 2018, after a total of three deferments. We believe that had the planning committee known what we now know then the scheme would not have been approved.

## Traders only 10%
Delancey's consented scheme is largely a residential development - it proposes nearly six times as much residential space as it does replacement retail (18k sqm & 106k sqm respectively)[^2]. 

![](http://35percent.org/img/delanceyshoppingcentrecgi.jpg)

Only 10% of the new retail space will be provided at affordable rates to accommodate existing independent traders who will pay 40 per cent of local market rates for a five year period and 75 per cent for the subsequent ten. This concession was only won from Delancey after a bitter campaign struggle. Delancey was originally offering only x%?? affordable retail and only discounted for the first 5 years. 

In any event it is clearly not enough - the Elephant's diverse community of independent traders make the place what it is and there will be no place for 90% of them if Delancey's plan is allowed to proceed.

![](http://35percent.org/img/traderscomp.png)

Nice concluding paragraph here with link to crowdjustice page.

Footnotes:

[^1]: Estates Gazzette article [published 13 March 1999](http://heygate.github.io/img/EstatesGazette.pdf)

[^2]: See paragraph 19 of the Officers report [insert link].

