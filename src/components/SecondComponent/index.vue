<template>
  <!-- 第一个 停电检测 -->
  <div>
    <!-- 二级标题 -->
    <dv-border-box-11 title="⚡️ 停电检测" style="width: 100%; height: 930px">
      <div>
        <!-- 三级标题 -->
        <div>
          <dv-border-box-5
            :color="['#225762', '#225762']"
            style="top: 80px; left: 40px; width: 280px; height: 40px"
          >
            <div
              style="
                padding-left: 15px;
                padding-top: 8px;
                font-size: 18px;
                font-weight: 700;
                color: #33ffff;
              "
            >
              ⚠️ 主网故障停电
            </div>
          </dv-border-box-5>
        </div>

        <div>
          <dv-border-box-8
            style="
              top: 90px;
              left: 40px;
              width: 820px;
              height: 340px;
              color: #fff;
            "
          >
            <div
              style="
                padding: 5px;
                font-size: 18px;
                font-weight: 700;
                color: #fff;
              "
            >
              <lineChart></lineChart>
            </div>
          </dv-border-box-8>
        </div>

        <!-- 下面 -->
        <div class="flex">
          <div>
            <!-- 三级标题 -->
            <div>
              <dv-border-box-5
                :color="['#225762', '#225762']"
                style="top: 120px; left: 40px; width: 280px; height: 40px"
              >
                <div
                  style="
                    padding-left: 15px;
                    padding-top: 8px;
                    font-size: 18px;
                    font-weight: 700;
                    color: #33ffff;
                  "
                >
                  ⚒️ 配电多维分析
                </div>
              </dv-border-box-5>
            </div>

            <div>
              <dv-border-box-8
                style="
                  top: 130px;
                  left: 40px;
                  width: 385px;
                  height: 340px;
                  color: #fff;
                "
              >
                <div
                  style="
                    padding: 5px;
                    font-size: 18px;
                    font-weight: 700;
                    color: #fff;
                  "
                >
                  <barChart></barChart>
                </div>
              </dv-border-box-8>
            </div>
          </div>

          <div style="margin-left: 40px">
            <!-- 三级标题 -->
            <div>
              <dv-border-box-5
                :color="['#225762', '#225762']"
                style="top: 120px; left: 40px; width: 280px; height: 40px"
              >
                <div
                  style="
                    padding-left: 15px;
                    padding-top: 8px;
                    font-size: 18px;
                    font-weight: 700;
                    color: #33ffff;
                  "
                >
                  💡 重点关注停电
                </div>
              </dv-border-box-5>
            </div>

            <div>
              <dv-border-box-8
                style="
                  top: 130px;
                  left: 40px;
                  width: 385px;
                  height: 340px;
                  color: #fff;
                "
              >
                <div
                  style="
                    padding: 10px;
                    font-size: 18px;
                    font-weight: 700;
                    color: #fff;
                  "
                >
                  <pieChart></pieChart>
                </div>
              </dv-border-box-8>
            </div>
          </div>
        </div>
      </div>
    </dv-border-box-11>
  </div>
</template>

<style lang="scss" scoped>
.flex {
  display: flex;
}
</style>



<script setup lang="ts">

import lineChart from "/@/components/SecondComponent/lineChart.vue";

import barChart from "/@/components/SecondComponent/barChart.vue";

import pieChart from "/@/components/SecondComponent/pieChart.vue";

</script>
