<template>
  <div class="content">
    <div class="md-layout">
      <div class="md-layout-item">
        <stats-card data-background-color="green">
          <template slot="header">
            <md-icon>code</md-icon>
          </template>

          <template slot="content">
            <h3>Code Security</h3>
            <img src="@/assets/img/apperture-red.png" style="width: 50%"/>
          <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Dynamic Code Analysis</span>
          </div>
          <div class="md-subhead">
            <md-icon style="color:red">error_outline</md-icon>
            <span>Static Code Analysis</span>
          </div>
          <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Vulnerability Assessment</span>
          </div>

                    </template>

        </stats-card>
      </div>
      <div class="md-layout-item" >
         <stats-card data-background-color="orange">
          <template slot="header">
            <md-icon>analytics</md-icon>
          </template>

          <template slot="content">
            <h3>Data Security</h3>
            <img src="@/assets/img/apperture-green.png" style="width: 50%"/>
          <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Classification</span>
          </div>
                    <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Static Code Analysis</span>
          </div>
                    <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Loss Prevention</span>
          </div>
          </template>

        </stats-card>       
      </div>
      <div class="md-layout-item" >
        <stats-card data-background-color="red">
          <template slot="header">
            <md-icon>dns</md-icon>
          </template>

          <template slot="content">
            <h3>Infrastructure Security</h3>
            <img src="@/assets/img/apperture-green.png" style="width: 50%"/>
          <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Container Protection</span>
          </div>
            <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Platform Hardening</span>
          </div>
            <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Secure Images</span>
          </div>
            </template>

        </stats-card>
      </div> 
      <div class="md-layout-item" >
        <stats-card data-background-color="gray">
          <template slot="header">
            <md-icon>engineering</md-icon>
          </template>

          <template slot="content">
            <h3>Integration Security</h3>
             <img src="@/assets/img/apperture-red.png" style="width: 50%"/>
         <div class="md-subhead">
            <md-icon style="color:green">task_alt</md-icon>
            <span>Authentication</span>
          </div>
          <div class="md-subhead">
            <md-icon style="color:red">error_outline</md-icon>
            <span>Exposure Protection</span>
          </div>
          <div class="md-subhead">
            <md-icon style="color:red">error_outline</md-icon>
            <span>Secure Protocols</span>
          </div>
          </template>

        </stats-card>
      </div>
            <div class="md-layout-item" >
        <stats-card data-background-color="blue">
          <template slot="header">
            <md-icon>dvr</md-icon>
          </template>

          <template slot="content">
            <h3>Operations Security</h3>
             <img src="@/assets/img/apperture-red.png" style="width: 50%"/>
          <div class="md-subhead">
            <md-icon style="color:red">error_outline</md-icon>
            <span>Access Monitoring</span>
          </div>             
          <div class="md-subhead">
            <md-icon style="color:red">error_outline</md-icon>
            <span>Log Centralization</span>
          </div>             
          </template>

        </stats-card>
      </div>
    </div>
  </div>
</template>

<script>
import {
  StatsCard,
 // NavTabsCard,
//  NavTabsTable,
 // OrderedTable,
} from "@/components";

export default {
  components: {
    StatsCard,
 //   NavTabsCard,
//    NavTabsTable,
 //   OrderedTable,
  },
  data() {
    return {
      dailySalesChart: {
        data: {
          labels: ["M", "T", "W", "T", "F", "S", "S"],
          series: [[12, 17, 7, 17, 23, 18, 38]],
        },
        options: {
          lineSmooth: this.$Chartist.Interpolation.cardinal({
            tension: 0,
          }),
          low: 0,
          high: 50, // creative tim: we recommend you to set the high sa the biggest value + something for a better look
          chartPadding: {
            top: 0,
            right: 0,
            bottom: 0,
            left: 0,
          },
        },
      },
      dataCompletedTasksChart: {
        data: {
          labels: ["12am", "3pm", "6pm", "9pm", "12pm", "3am", "6am", "9am"],
          series: [[67, 75, 80, 100, 99, 80, 100, 100]],
        },

        options: {
          lineSmooth: this.$Chartist.Interpolation.cardinal({
            tension: 0,
          }),
          low: 0,
          high: 120, // creative tim: we recommend you to set the high sa the biggest value + something for a better look
          chartPadding: {
            top: 0,
            right: 0,
            bottom: 0,
            left: 0,
          },
        },
      },
      emailsSubscriptionChart: {
        data: {
          labels: [
            "Ja",
            "Fe",
            "Ma",
            "Ap",
            "Mai",
            "Ju",
            "Jul",
            "Au",
            "Se",
            "Oc",
            "No",
            "De",
          ],
          series: [
            [542, 443, 320, 780, 553, 453, 326, 434, 568, 610, 756, 895],
          ],
        },
        options: {
          axisX: {
            showGrid: false,
          },
          low: 0,
          high: 1000,
          chartPadding: {
            top: 0,
            right: 5,
            bottom: 0,
            left: 0,
          },
        },
        responsiveOptions: [
          [
            "screen and (max-width: 640px)",
            {
              seriesBarDistance: 5,
              axisX: {
                labelInterpolationFnc: function (value) {
                  return value[0];
                },
              },
            },
          ],
        ],
      },
    };
  },
};
</script>
