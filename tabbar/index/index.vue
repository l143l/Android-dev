<template>
  <view class="content">
    <!-- 顶部标题栏 -->
    <view class="header">
      <view class="header-inner">
        <text class="header-text">使用说明大全</text>
      </view>
    </view>

    <!-- 图片网格布局 -->
    <view class="image-grid">
      <view class="image-item" @click="goPage('app1')">
        <image class="img" src="/static/wx_rounded.png" mode="aspectFill"></image>
        <text class="img-label">微信使用指南</text>
      </view>
      <view class="image-item" @click="goPage('app2')">
        <image class="img" src="/static/jd_rounded.png" mode="aspectFill"></image>
        <text class="img-label">京东使用指南</text>
      </view>
      <view class="image-item" @click="goPage('app3')">
        <image class="img" src="/static/tb_rounded.png" mode="aspectFill"></image>
        <text class="img-label">淘宝使用指南</text>
      </view>
      <view class="image-item" @click="goPage('app4')">
        <image class="img" src="/static/dy_rounded.png" mode="aspectFill"></image>
        <text class="img-label">抖音使用指南</text>
      </view>
      <!-- 新增的优酷入口 -->
      <view class="image-item" @click="goPage('app5')">
        <image class="img" src="/static/yk.png" mode="aspectFill"></image>
        <text class="img-label">优酷使用指南</text>
      </view>
    </view>

    <!-- 底部反馈按钮 -->
    <view class="footer" @click="goFeedback">
      <text class="feedback-text">使用反馈</text>
      <image class="feedback-icon" src="/static/feedback-icon.png" mode="widthFix"></image>
    </view>
  </view>
</template>

<script>
export default {
  methods: {
    goPage(pageName) {
      uni.navigateTo({
        url: `/pages/tabbar/${pageName}/${pageName}`
      });
    },
    goFeedback() {
      const url = 'https://v.wjx.cn/vm/mHymBaH.aspx#';
      // #ifdef H5
      window.open(url, '_blank');
      // #endif

      // #ifdef APP-PLUS
      plus.runtime.openURL(url);
      // #endif

      // #ifdef MP-WEIXIN
      wx.navigateTo({
        url: '/pages/webview/webview?src=' + encodeURIComponent(url)
      });
      // #endif
    }
  }
};
</script>

<style scoped>
/* 全局样式 */
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #fff8e0;
  height: 100vh;
  padding-bottom: 120rpx;
  box-sizing: border-box;
}

/* 顶部标题栏 */
.header {
  width: 100%;
  background: linear-gradient(135deg, #ffdfa6 0%, #ffc88a 100%);
  padding: 40rpx 0;
  box-shadow: 0 4rpx 12rpx rgba(231, 127, 0, 0.15);
  position: relative;
  overflow: hidden;
}

.header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: radial-gradient(circle, rgba(255,255,255,0.15) 1px, transparent 1px);
  background-size: 30rpx 30rpx;
}

.header-inner {
  width: 100%;
  text-align: center;
  position: relative;
  z-index: 1;
}

.header-text {
  font-size: 44rpx;
  font-weight: 600;
  color: #e77f00;
  letter-spacing: 2rpx;
  text-shadow: 0 2rpx 4rpx rgba(0,0,0,0.05);
}

/* 图片网格布局 - 保持原有样式 */
.image-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60rpx;
  width: 85%;
  margin-top: 100rpx;
}

/* 图片项容器 */
.image-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20rpx;
  transition: transform 0.3s ease;
}

.image-item:active {
  transform: scale(0.95);
}

/* 图片样式 */
.img {
  width: 240rpx;
  height: 240rpx;
  border-radius: 20rpx;
  box-shadow: 0 8rpx 24rpx rgba(231, 127, 0, 0.2);
  transition: all 0.3s ease;
  overflow: hidden;
  position: relative;
}

.img::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(255,255,255,0.05);
  transition: all 0.3s ease;
}

.image-item:hover .img {
  transform: translateY(-8rpx);
  box-shadow: 0 12rpx 32rpx rgba(231, 127, 0, 0.3);
}

.image-item:hover .img::after {
  background: rgba(255,255,255,0.1);
}

/* 图片标签 */
.img-label {
  font-size: 32rpx;
  color: #e77f00;
  font-weight: 500;
  text-shadow: 0 2rpx 4rpx rgba(0,0,0,0.05);
  letter-spacing: 1rpx;
}

/* 底部反馈按钮 */
.footer {
  width: 75%;
  background: linear-gradient(135deg, #ff874f 0%, #ff6b2b 100%);
  color: white;
  padding: 24rpx 0;
  border-radius: 60rpx;
  text-align: center;
  font-size: 36rpx;
  font-weight: 500;
  box-shadow: 0 8rpx 24rpx rgba(255, 135, 79, 0.3);
  position: fixed;
  bottom: 60rpx;
  left: 50%;
  transform: translateX(-50%);
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16rpx;
  letter-spacing: 2rpx;
}

.footer:active {
  transform: translateX(-50%) scale(0.96);
  box-shadow: 0 4rpx 16rpx rgba(255, 135, 79, 0.2);
}

.feedback-text {
  color: white;
  font-size: 36rpx;
  font-weight: 500;
}

.feedback-icon {
  width: 36rpx;
  height: auto;
  filter: brightness(0) invert(1);
}

/* 适配不同屏幕尺寸 */
@media (max-width: 320px) {
  .image-grid {
    gap: 40rpx;
  }
  
  .img {
    width: 200rpx;
    height: 200rpx;
  }
}

@media (min-width: 414px) {
  .image-grid {
    gap: 80rpx;
  }
  
  .img {
    width: 260rpx;
    height: 260rpx;
  }
}
</style>