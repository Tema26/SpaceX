<template>
  <div class="flight-list__item" v-for="card in cards" :key="card.mission + card.title">
      <img class="flight-list__item-img" :src="card.logo" :alt="card.title">
      <div class="flight-list__item-info">
            <div class="flight-list__item-info-mission">{{ card.mission }}</div>
            <h2 class="flight-list__item-info-title">{{ card.title }}</h2>
            <p class="flight-list__item-info-text">{{ card.text }}</p>
            <div class="flight-list__item-info-data">
                <div class="flight-list__item-info-data-wrapper">
                    <img src="@/assets/images/calendar.png" alt="calendar" class="flight-list__item-info-data-wrapper-img">
                    <span class="flight-list__item-info-data-wrapper-text">{{ card.data.fullData }}</span>
                </div>
                <div class="flight-list__item-info-data-wrapper">
                    <img src="@/assets/images/time.png" alt="time" class="flight-list__item-info-data-wrapper-img">
                    <span class="flight-list__item-info-data-wrapper-text">{{ card.data.time }}</span>
                </div>
                <div class="flight-list__item-info-data-wrapper">
                    <img src="@/assets/images/rocket.png" alt="rocket" class="flight-list__item-info-data-wrapper-img">
                <span class="flight-list__item-info-data-wrapper-text">{{ card.rocket }}</span>
                </div>
            </div>
      </div>
  </div>
</template>

<script>
export default {
    props: ['cards']
}
</script>

<style lang="scss">
@import '../styles/_variables';
    .flight-list__item {
        background: rgba(34, 36, 43, 0.8);
        margin-top: 20px;
        display: grid;
        grid-template-columns: 25% 75%;
        padding: 50px;
        &:first-child {
            margin-top: 0;
        };
        &-img {
            display: block;
            margin: 0 auto;
            max-width: 90%;
        }
        &-info {
            &-mission {
                color: $colorBlue;
                font-weight: 400;
                letter-spacing: 7px;
            }
            &-title {
                font-size: 72px;
                margin: 10px 0;
            }
            &-data {
                margin-top: 20px;
                display: flex;
                &-wrapper {
                    display: flex;
                    align-items: center;
                    &-img {
                        margin-left: 7px;
                    }
                    &-text {
                        margin-left: 5px;
                    }
                }
            }
        }
    }
</style>