<template>
  <view class="page">
    <!-- 顶部标题栏 -->
    <view class="header">
      <view class="back-btn" @click="goBack">← 返回</view>
      <view class="title">抖音使用说明</view>
    </view>

    <!-- 可滚动内容 -->
    <scroll-view class="content" scroll-y="true">
      <view class="section">
        <view class="text">
          <text decode="true">
            1、如何搜索相关话题\n 
            2、如何加关注\n
            3、如何发布视频\n
            下面进行详细介绍：
          </text>
        </view>
      </view>

      <view class="section">
        <view class="section-title">1、如何搜索相关话题</view>
        
        <view class="text">
          在输入框中输入要搜索的话题，点击"搜索"
        </view>
        
        <view class="image">
          <image class="img" src="/static/4.1.png" mode="widthFix"></image>
        </view>
      </view>

      <view class="section">
        <view class="section-title">2、如何加关注</view>
        
        <view class="text">
          刷视频过程中，遇到喜欢的博主或话题点击右侧"+"关注博主
        </view>
        
        <view class="image-row">
          <image class="img" src="/static/1.5.png" mode="widthFix"></image>
          <image class="img" src="/static/1.6.png" mode="widthFix"></image>
        </view>
      </view>
      
      <view class="section">
        <view class="section-title">3、如何发布视频</view>
        
        <view class="text">
          点击底部中间的"+" → 点击"拍摄"或"相册" → 选择或拍摄视频 → 添加特效和音乐 → 编辑描述 → 点击"发布"
        </view>
        
        <view class="image-row">
          <image class="img" src="/static/1.7.png" mode="widthFix"></image>
          <image class="img" src="/static/1.8.png" mode="widthFix"></image>
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

/* 图片并排排列 */
.image-row {
  display: flex;
  justify-content: space-between;
  gap: 30rpx;
  margin-top: 40rpx;
}

.image-row .img {
  flex: 1;
}

/* 图片样式 */
.img {
  width: 100%;
  border-radius: 20rpx;
  background-color: #f8f8f8;
  margin-bottom: 30rpx;
  box-shadow: 0 4rpx 16rpx rgba(0, 0, 0, 0.1);
}

/* 单张图片容器 */
.image {
  margin-top: 20rpx;
}

/* 文本说明 - 增大字体适合老年人 */
.text {
  font-size: 38rpx;
  line-height: 1.8;
  color: #333;
  text-align: left;
  letter-spacing: 1rpx;
}

.text text {
  font-size: 38rpx;
  line-height: 2;
}
</style>