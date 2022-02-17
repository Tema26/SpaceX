<template>
  <header class="header">
    <img class="header__logo" src="./assets/images/spacex-logo.png">
    <h1 class="header__title">Space <span class="header__title_white">X</span> <span class="header__title_newline">Missions</span></h1>
  </header>
  <section class="flight-list">
    <card-starting :cards="cards"/>
  </section>
</template>

<script>
import CardStarting from './components/CardStarting.vue'

export default {
  name: 'App',
  components: {
    CardStarting
  },
  data() {
    return {
      cards: [
        {
          mission: 'Mission 1',
          logo: './images/saocom.png',
          title: 'SAOCOM 1B, GNOMES-1, Tyvak-0172',
          text: "SpaceX's Falcon 9 will launch the second of the two satellite SAOCOM 1 satellites into a sun-synchronous polar orbit from SLC-40, Cape Canaveral AFS. SAOCOM 1B is a synthetic aperture radar Earth observation satellite to support disaster management. \n\n The SAOCOM spacecraft are operated by CONAE, the Argentinian National Space Activities Commission, and are built by INVAP. This mission is also expected to include rideshare payloads Sequoia, and GNOMES-1. This will be the first polar launch from the Space Coast in 60 years. The launch azimuth will be southward and the booster will land at LZ-1.",
          data: {
            fullData: '2020-08-30',
            time: '23:18:00'
          },
          rocket: 'Falcon 9'
        },
        {
          mission: 'Mission 2',
          logo: './images/starlink.png',
          title: 'Starlink-12 (v1.0)',
          text: 'This mission will launch the twelfth batch of operational Starlink satellites, which are expected to be version 1.0, from SLC-40, Cape Canaveral Air Force Station. It is the thirteenth Starlink launch overall. The satellites will be delivered to low Earth orbit and will spend a few weeks maneuvering to their operational altitude of 550 km. The booster for this mission is expected to land on an ASDS',
          data: {
            fullData: '2020-10-06',
            time: '11:29:00'
          },
          rocket: 'Falcon 9'
        },
        {
          mission: 'Mission 3',
          logo: './images/crew.png',
          title: 'Crew-1',
          text: "SpaceX will launch the first operational mission of its Crew Dragon vehicle as part of NASA's Commercial Crew Transportation Capability Program (CCtCap), carrying 3 NASA astronauts and 1 JAXA astronaut to the International Space Station. This mission will be the second crewed flight to launch from the United States since the end of the Space Shuttle program in 2011",
          data: {
            fullData: '2020-11-16',
            time: '00:27:00'
          },
          rocket: 'Falcon 9'
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import './styles/_global';
@import './styles/blocks/_header';
@import './styles/_mediaQuery';
</style>
