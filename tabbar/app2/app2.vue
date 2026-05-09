<template>
  <view class="page">
    <!-- 顶部标题栏 -->
    <view class="header">
      <view class="back-btn" @click="goBack">← 返回</view>
      <view class="title">京东使用说明</view>
    </view>

    <!-- 可滚动内容 -->
    <scroll-view class="content" scroll-y="true">
      <view class="section">
        <view class="text">
          <text decode="true">
            1、如何调整为长辈模式\n
            2、如何设置收货地址\n
            3、如何购买想要的商品\n
            下面进行详细介绍：
          </text>
        </view>
      </view>

      <view class="section">
        <view class="section-title">1、如何调整为长辈模式</view>
        
        <view class="text">
          （1）打开京东APP后进入下方界面，点击"我的"
        </view>

        <view class="image">
          <image class="img" src="/static/3.1.jpg" mode="widthFix"></image>
        </view>
      </view>

      <view class="section">
        <view class="text">
          （2）进入"我的"界面后，点击"设置"
        </view>
        
        <view class="image">
          <image class="img" src="/static/3.2.png" mode="widthFix"></image>
        </view>
      </view>
      
      <view class="section">
        <view class="text">
          （3）进入下方界面后，点击"模式切换"
        </view>
        
        <view class="image">
          <image class="img" src="/static/3.3.png" mode="widthFix"></image>
        </view>
      </view>
      
      <view class="section">
        <view class="text">
          （4）点击"长辈模式"即完成切换
        </view>
        
        <view class="image">
          <image class="img" src="/static/3.4.jpg" mode="widthFix"></image>
        </view>
      </view>
    </scroll-view>
  </view>
</template>

<script>
export default {
  methods: {
    goBack() {
      uni.navigateBack();
    }
  }
};
</script>

<style>
.page {
  display: flex;
  flex-direction: column;
  height: 100vh;
  background-color: #fff8e0;
}

/* 顶部标题栏 */
.header {
  position: relative;
  width: 100%;
  text-align: center;
  font-size: 48rpx;
  font-weight: bold;
  padding: 40rpx 0;
  background: linear-gradient(135deg, #ffdfa6 0%, #ffc88a 100%);
  color: #e77f00;
  box-shadow: 0 4rpx 12rpx rgba(231, 127, 0, 0.15);
}

/* 返回按钮样式（左上角） */
.back-btn {
  position: absolute;
  left: 40rpx;
  top: 50%;
  transform: translateY(-50%);
  padding: 20rpx 30rpx;
  background-color: #fff6e5;
  border-radius: 12rpx;
  color: #e77f00;
  font-size: 36rpx;
  font-weight: 500;
  box-shadow: 0 4rpx 8rpx rgba(0, 0, 0, 0.1);
}

/* 标题文本单独居中 */
.title {
  text-align: center;
}

/* 滚动内容区 */
.content {
  flex: 1;
  padding: 40rpx;
  box-sizing: border-box;
}

/* 内容块 */
.section {
  margin-bottom: 80rpx;
  background: white;
  border-radius: 24rpx;
  padding: 40rpx;
  box-shadow: 0 8rpx 24rpx rgba(0, 0, 0, 0.08);
}

/* 章节标题 */
.section-title {
  font-size: 44rpx;
  font-weight: 600;
  color: #e77f00;
  margin-bottom: 30rpx;
  padding-bottom: 20rpx;
  border-bottom: 4rpx solid #ffdfa6;
}

/* 图片样式 */
.img {
  width: 100%;
  border-radius: 20rpx;
  background-color: #f8f8f8;
  margin-bottom: 30rpx;
  box-shadow: 0 4rpx 16rpx rgba(0, 0, 0, 0.1);
}

/* 文本说明 - 增大字体适合老年人 */
.text {
  font-size: 38rpx;
  line-height: 1.8;
  color: #333;
  text-align: left;
  letter-spacing: 1rpx;
  margin-bottom: 20rpx;
}

.text text {
  font-size: 38rpx;
  line-height: 2;
}

/* 图片容器 */
.image {
  margin-top: 20rpx;
}
</style>