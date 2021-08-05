<template>
  <div class="container-wrap">
    <div class="container">
      <div class="content" v-for="vedio in vedios" :key="vedio.title">
        <div class="image-wrap">
          <img class="image" :src="vedio.image" />
          <div class="time-wrap">
            <div class=" totletime">
              {{ vedio.totletime }}
            </div>
          </div>
        </div>
        <div class="title">{{ vedio.title }}</div>
        <div class="views">{{ vedio.views }}</div>
      </div>
      <div class="bottom-space">bottom-space</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      vedios: [
        {
          title: "羽球男雙奪金, 麟洋配返台! 爸接機喊愛你| TVBS 新聞",
          editor: "TVBS NEWS",
          views: "觀看次數:1860次 . 2小時前",
          totletime: "1:48",
          image: `${require(`../assets/img/01.jpg`)}`
        },
        {
          title:
            "【自然の音と4K 映像】夏を涼しく過ごす 湧水の里　円原川の水中 3時間",
          editor: "kazephoto _ 4 K",
          views: "觀看次數：850,236次. 2小時前",
          totletime: "05:48:12",
          image: `${require(`../assets/img/02.jpg`)}`
        },
        {
          title: "陳奎儒賽後落淚 真的好想拚進決賽/愛爾達電視20210804",
          editor: "爾達體育家族 ELTA Sports",
          views: "觀看次數：75,858次. 7小時前",
          totletime: "2:18",
          image: `${require(`../assets/img/11.jpg`)}`
        },
        {
          title: "世界十大最危險的工作和收入 | 老高與小茉 Mr & Mrs Gao",
          editor: "老高與小茉 Mr & Mrs Gao",
          views: "觀看次數：103,200次 . 9小時前",
          totletime: "20:38",
          image: `${require(`../assets/img/04.jpg`)}`
        },
        {
          title:
            "五局上 王維中連飆2K ! 化解滿壘失分危機 ! 8/4 (三) 富邦 vs 味全【中華職棒】",
          editor: "ELEVEN TAIWAN",
          views: "觀看次數：464次 . 1小時前",
          totletime: "3:38",
          image: `${require(`../assets/img/05.jpg`)}`
        },
        {
          title:
            "Laravel PHP Framework Tutorial - Full Course for Beginners (2019)",
          editor: "freeCodeCamp.org",
          views: "觀看次數：1,424,865次 . 12小時前",
          totletime: "04:15:48",
          image: `${require(`../assets/img/06.jpg`)}`
        },
        {
          title:
            "Rainy Jazz: Relaxing Jazz & Bossa Nova Music Radio - 24/7 Chill Out Piano & Guitar Music",
          editor: "Cafe Music BGM channel",
          views: "927人正在觀看 . 直播中",
          totletime: "15:48",
          image: `${require(`../assets/img/02.jpg`)}`
        },
        {
          title:
            "【2021爪嗨賴】08/04 陳子豪炸裂超兇逆轉兩分砲，峮峮帶大家一起應援！CTBC Brothers 中信兄弟",
          editor: "CTBC Brothers 中信兄弟官方頻道",
          views: "觀看次數:3780次 . 9小時前",
          totletime: "1:46",
          image: `${require(`../assets/img/08.jpg`)}`
        },
        {
          title: "周杰倫 Jay Chou【夜曲 Nocturne】Official Music Video",
          editor: "周杰倫 Jay Chou",
          views: "觀看次數:40112176次 . 2小時前",
          totletime: "3:53",
          image: `${require(`../assets/img/09.jpg`)}`
        },
        {
          title: "不忍了 正式回應酸民對我的指責。",
          editor: "蒼藍鴿的醫學天地",
          views: "觀看次數:191677次 . 7小時前",
          totletime: "8:53",
          image: `${require(`../assets/img/10.jpg`)}`
        },
        {
          title:
            "猜猜那個白飯最好吃？進口的、超商的、還是自己隨便煮的？ Microwavable Rice",
          editor: "壹加壹",
          views: "觀看次數:7336次 . 2小時前",
          totletime: "10:00",
          image: `${require(`../assets/img/11.jpg`)}`
        },
        {
          title: "在你身邊為你加油，這樣的滋味，真好",
          editor: "麥當勞官方頻道",
          views: "觀看次數:12308次 . 2天前",
          totletime: "7:13",
          image: `${require(`../assets/img/12.jpg`)}`
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.container {
  transform: translateY(15vh);
  height: 93vh;

  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 1rem;
  z-index: -1;
  background: rgba(238, 238, 238, 0.644);
}

.image-wrap {
  position: relative;
  cursor: pointer;
  &:hover {
    .time-wrap {
      transition: opacity 0.3s ease;
      opacity: 0;
    }
  }

  .image {
    width: 100%;
  }
  .time-wrap {
    background-color: black;
    color: white;
    width: 60px;
    text-align: center;
    padding: 2px;
    position: absolute;
    bottom: 5px;
    right: 0;
  }
}
.bottom-space {
  width: 100%;
  height: 6vh;
}

@media screen and (min-width: 550px) {
  .container {
    grid-template-columns: 1fr 1fr;
  }
}
@media screen and (min-width: 960px) {
  .container {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
@media screen and (min-width: 1260px) {
  .container {
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }
}
</style>
