<template>
  <view class="page">
    <!-- 顶部标题栏 -->
    <view class="header">
      <view class="back-btn" @click="goBack">← 返回</view>
      <view class="title">优酷视频使用说明</view>
    </view>

    <!-- 可滚动内容 -->
    <scroll-view class="content" scroll-y="true">
      <view class="section">
        <view class="text">
          <text decode="true">
            1、如何搜索想看的视频\n
            2、如何播放视频和调节播放设置\n
            3、如何收藏喜欢的视频\n
            4、如何查看观看历史\n
            5、如何调整视频清晰度\n
            6、如何开启和关闭弹幕\n
            下面进行详细介绍：
          </text>
        </view>
      </view>

      <view class="section">
        <view class="section-title">1、如何搜索想看的视频</view>
        
        <view class="text">
          第一步：打开优酷APP，在首页顶部可以看到搜索框\n
          第二步：点击搜索框，输入您想看的视频名称或关键词\n
          第三步：点击键盘上的"搜索"按钮或右侧的搜索图标\n
          第四步：在搜索结果中找到您想看的视频，点击即可播放\n
          温馨提示：如果不知道具体名字，可以输入类型如"抗战电视剧"或"搞笑小品"等
        </view>
      </view>

      <view class="section">
        <view class="section-title">2、如何播放视频和调节播放设置</view>
        
        <view class="text">
          播放视频操作：\n
          1. 找到想看的视频后，直接点击视频封面图片\n
          2. 视频开始播放后，屏幕下方会出现播放控制条\n
          \n
          播放控制功能介绍：\n
          ▶️ 播放/暂停按钮：点击中间可以暂停或继续播放\n
          ⏪⏩ 快退快进：点击左右两侧可以前进或后退15秒\n
          🔊 音量调节：点击音量图标或按手机音量键调节\n
          📱 全屏观看：点击全屏图标可以横屏全屏观看\n
          ⏸️ 倍速播放：点击倍速可以调整播放速度（0.5x-2.0x）
        </view>
      </view>
      
      <view class="section">
        <view class="section-title">3、如何收藏喜欢的视频</view>
        
        <view class="text">
          第一步：在视频播放页面，点击屏幕中间唤出控制条\n
          第二步：在视频右下角找到"收藏"按钮（通常是心形图标）\n
          第三步：点击"收藏"按钮，按钮变色表示收藏成功\n
          第四步：想查看收藏的视频，可以点击底部"我的"→"我的收藏"\n
          温馨提示：收藏后即使视频下架，只要在收藏期内都能观看
        </view>
      </view>

      <view class="section">
        <view class="section-title">4、如何查看观看历史</view>
        
        <view class="text">
          查看观看历史记录方法：\n
          方法一：在首页向下滑动，找到"观看历史"栏目\n
          方法二：点击底部"我的"选项卡，然后点击"观看历史"\n
          \n
          管理观看历史：\n
          1. 清空历史：点击页面右上角的"清空"按钮\n
          2. 删除单条：向左滑动某条记录，点击"删除"\n
          3. 继续观看：点击历史记录中的视频，会从上次观看位置继续
        </view>
      </view>

      <view class="section">
        <view class="section-title">5、如何调整视频清晰度</view>
        
        <view class="text">
          调整清晰度步骤：\n
          1. 在视频播放页面，点击屏幕中间\n
          2. 点击右上角的"清晰度"或"画质"按钮\n
          3. 在弹出的选项中选择适合的清晰度：\n
             - 流畅：节省流量，适合网络不好时\n
             - 标清：普通清晰度，平衡画质和流量\n
             - 高清：较清晰的画质\n
             - 超清：最清晰的画质，需要较好网络\n
          4. 选择后会自动切换，等待几秒缓冲即可
        </view>
      </view>

      <view class="section">
        <view class="section-title">6、如何开启和关闭弹幕</view>
        
        <view class="text">
          弹幕操作指南：\n
          开启弹幕：\n
          1. 播放视频时，点击屏幕中间\n
          2. 找到弹幕开关按钮（通常在屏幕右上角）\n
          3. 点击弹幕按钮，按钮亮起表示弹幕已开启\n
          \n
          关闭弹幕：\n
          再次点击弹幕按钮，按钮变灰表示弹幕已关闭\n
          \n
          调节弹幕设置：\n
          1. 弹幕透明度：可以调节弹幕的透明程度\n
          2. 弹幕大小：可以调节弹幕字体大小\n
          3. 弹幕速度：可以调节弹幕滚动速度\n
          4. 屏蔽关键词：可以屏蔽不想看到的弹幕内容
        </view>
      </view>

      <view class="section">
        <view class="section-title">温馨提示</view>
        
        <view class="text">
          1. 观看视频时请注意休息，每隔45分钟让眼睛休息一下\n
          2. 使用WiFi观看高清视频可以节省手机流量\n
          3. 遇到卡顿时可以尝试降低清晰度或暂停缓冲一会儿\n
          4. 夜间观看可以开启护眼模式或调低屏幕亮度\n
          5. 如有任何问题，可以联系优酷客服热线：400-810-0580
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
  margin-bottom: 60rpx;
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