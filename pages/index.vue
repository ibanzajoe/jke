<template>
  <div class="main-grid">
    <div class="grid-hero">
      <hero />
    </div>
    <div class="grid-services">
      <divider />
      <div class="grid-services-title">
        Services
      </div>
      <services :services="jkeData.services"
      />
    </div>
    <div class="grid-booking">
      <divider />
      <div class="grid-booking-title">
        Book a Hair Appointment
      </div>
      <booking :bookings="jkeData.bookings" />

    </div>
    <div class="grid-style">

    </div>
    <div class="grid-contact">

    </div>
    <div class="grid-footer">

    </div>
  </div>
</template>

<script>
import hero from '~/components/landing/hero'
import divider from '~/components/divider'
import services from '~/components/landing/services'
import booking from '~/components/landing/booking'

export default {
  components: {
    hero,divider, services, booking
  },
  data () {
    return {
      jkeData: {
        hero: {
          hero_title: 'Hair By JKE',
          hero_image_url: 'https://img1.wsimg.com/isteam/ip/bcc5efe4-5bfe-45c7-8f45-5dc2ca01c600/1a6eb00f-1e98-46f4-989b-2bfcc8f93422.jpg/:/cr=t:0%25,l:0%25,w:100%25,h:100%25/rs=w:1050,cg:true',
          hero_background_splash_text: 'Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE Hair By JKE ',
          hero_content_heading: 'Welcome to Hair By JKE',
          hero_content_subheading: 'Our expert stylists will help you shine!'
        },
        services: [
          {
            type: 'Haircut',
            description: 'Keep your hair looking fresh and trimmed',
            items: [
              {
                image: '../images/womenhaircut.webp',
                label: "Women's Haircut and Blowdry",
                price: '$90+'
              },
              {
                image: '../images/menshaircut.webp',
                label: "Man's Haircut",
                price: '$80+'
              },
              {
                image: '../images/misccut.webp',
                label: '',
                price: ''
              }
            ]
          },
          {
            type: 'Coloring',
            description: 'High-quality coloring products and friendly, professional service',
            items: [
              {
                image: '../images/partialhighlight.webp',
                label: 'Partial Highlights',
                price: '155+'
              },
              {
                image: '../images/single.webp',
                label: 'Single Process Color',
                price: '95+'
              },
              {
                image: '../images/misccolor.webp',
                label: '',
                price: ''
              }
            ]
          }
        ],
        bookings: [
          {
            type: 'Haircut',
            description: 'Men/Women Starts at $80.00',
            price: '$80',
            time: '1 hr'
          },
          {
            type: 'Blowdry',
            description: 'Blowdry + Curling iron(Style) $75.00',
            price: '$55.00',
            time: '1 hr'
          },
          {
            type: 'Event Styling',
            description: 'Event Styling',
            price: '$100',
            time: '1 hr'
          }
        ]

      }
    }
  }
}
</script>

<style scoped>
  .main-grid {
    max-width: 1440px;
    margin: 0 auto;
    display: grid;
    grid-template-rows: auto;
  }

  .grid-services-title, .grid-booking-title {
    font-size: 49px;
    line-height: 1.4;
    color: rgb(95, 11, 53);
    font-weight: 400;
    overflow-wrap: break-word;

    text-align: center;
  }
</style>
