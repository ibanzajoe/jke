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
      <div class="grid-booking-banner">
        <div class="banner-block">
          <svg viewBox="0 0 24 24" fill="currentColor" width="48px" height="48px" data-ux="Icon" class="x-el x-el-svg c1-27 c1-4x c1-9n c1-9o c1-9p c1-9q c1-2b c1-25 c1-9r c1-9s c1-9t c1-9u c1-9v c1-9w c1-9x c1-9y c1-2h c1-2i x-d-ux"><path d="M14.667 12a2.57 2.57 0 0 0-.782-1.885A2.57 2.57 0 0 0 12 9.333a2.57 2.57 0 0 0-1.885.782A2.57 2.57 0 0 0 9.333 12c0 .736.26 1.365.782 1.885.52.521 1.149.782 1.885.782a2.57 2.57 0 0 0 1.885-.782c.521-.52.782-1.149.782-1.885zm1.437 0c0 1.139-.4 2.108-1.198 2.906-.798.799-1.767 1.198-2.906 1.198-1.139 0-2.108-.4-2.906-1.198-.799-.798-1.198-1.767-1.198-2.906 0-1.139.4-2.108 1.198-2.906.798-.799 1.767-1.198 2.906-1.198 1.139 0 2.108.4 2.906 1.198.799.798 1.198 1.767 1.198 2.906zm1.125-4.27c0 .263-.094.489-.281.676a.923.923 0 0 1-.677.282.923.923 0 0 1-.677-.282.923.923 0 0 1-.281-.677c0-.264.093-.49.28-.677a.923.923 0 0 1 .678-.281c.264 0 .49.094.677.281a.923.923 0 0 1 .281.677zM12 5.437l-.797-.006a56.514 56.514 0 0 0-1.099 0c-.25.004-.585.014-1.005.032-.42.017-.778.052-1.073.104a4.177 4.177 0 0 0-.745.192c-.347.14-.653.34-.916.605-.264.263-.466.569-.605.916-.076.202-.14.45-.192.745a8.255 8.255 0 0 0-.104 1.073c-.018.42-.028.755-.032 1.005-.003.25-.003.616 0 1.1l.006.796-.006.797c-.003.483-.003.849 0 1.099.004.25.014.585.032 1.005.017.42.052.778.104 1.073.052.295.116.543.192.745.14.347.34.653.605.916.263.264.569.466.916.605.202.076.45.14.745.192.295.052.653.087 1.073.104.42.018.755.028 1.005.032.25.003.616.003 1.1 0l.796-.005.797.005c.483.003.849.003 1.099 0 .25-.004.585-.014 1.005-.032.42-.017.778-.052 1.073-.104.295-.052.543-.116.745-.192.347-.14.653-.34.916-.605.264-.263.466-.569.605-.916.076-.202.14-.45.192-.745.052-.295.087-.653.104-1.073.018-.42.028-.755.032-1.005.003-.25.003-.616 0-1.1L18.562 12l.006-.797c.003-.483.003-.849 0-1.099a38.59 38.59 0 0 0-.032-1.005 8.255 8.255 0 0 0-.104-1.073 4.177 4.177 0 0 0-.192-.745 2.703 2.703 0 0 0-.605-.916 2.703 2.703 0 0 0-.916-.605 4.177 4.177 0 0 0-.745-.192 8.255 8.255 0 0 0-1.073-.104c-.42-.018-.755-.028-1.005-.032-.25-.003-.616-.003-1.1 0L12 5.438zM20 12c0 1.59-.017 2.691-.052 3.302-.07 1.445-.5 2.563-1.292 3.354-.791.792-1.91 1.222-3.354 1.292-.611.035-1.712.052-3.302.052s-2.691-.017-3.302-.052c-1.445-.07-2.563-.5-3.354-1.292-.792-.791-1.222-1.91-1.292-3.354C4.017 14.691 4 13.59 4 12s.017-2.691.052-3.302c.07-1.445.5-2.563 1.292-3.354.791-.792 1.91-1.222 3.354-1.292C9.309 4.017 10.41 4 12 4s2.691.017 3.302.052c1.445.07 2.563.5 3.354 1.292.792.791 1.222 1.91 1.292 3.354.035.611.052 1.712.052 3.302z"></path></svg>
        </div>
      </div>

      <divider />

      <div class="carousel-container">
        <v-carousel hide-delimiters>
          <v-carousel-item
            class="carousel-item-holder"
            v-for="(item,i) in jkeData.styleImages"
            :key="i"
            :src="item"
          >



          </v-carousel-item>
        </v-carousel>
      </div>

    </div>

    <div class="grid-contact">
      <divider />
      <contact :contact="jkeData.contact" />
      <!--<pre>{{jkeData.contact}}</pre>-->
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
import contact from '~/components/landing/contact'

export default {
  components: {
    hero,divider, services, booking, contact
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
        ],
        styleImages: [
          './images/image1.webp',
          './images/image2.webp',
          './images/image3.webp',
          './images/image4.webp',
          './images/image5.webp',
          './images/image6.webp'
        ],
        contact: {
          headers: {
            heading: 'Stay on the cutting-edge',
            subheading: 'Sing up to hear from us about specials, sales, events, and fashion tips.'
          },
          map: {

          },
          content: [
            {
              heading: 'Cancellation Policy',
              content: 'Cancellations accepted up to 24 hours before the scheduled service. Within 24 hours of the service, cancellations will be charged 50% of the scheduled cost.'
            },
            {
              heading: 'Hair By JKE',
              content: '9666 Brighton Way, Beverly Hills, California 90210',
              phone: '(213) 200 2940'
            },
            {
              heading: 'Hours',
              content: 'time',
              time: [
                'Tuesday 10 am to 5 pm',
                'Wednesday 10 am to 5pm',
                'Thursday 10 am to 5 pm',
                'Friday 10 am to 5 pm',
                'Saturday 8 am to 4 pm'
              ]
            }
          ]
        }

      }
    }
  }
}
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
  .main-grid {
    max-width: 1440px;
    margin: 0 auto;
    display: grid;
    grid-template-rows: auto;
    background-color: #fff;
    padding-bottom: 5rem;
  }

  .grid-services-title, .grid-booking-title {
    font-size: 49px;
    line-height: 1.4;
    color: rgb(95, 11, 53);
    font-weight: 400;
    overflow-wrap: break-word;

    text-align: center;
  }

  .grid-booking-banner {
    padding-top: 70px;
    padding-bottom: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .banner-block {

  }

  .banner-block svg {
    color: rgb(95, 11, 53);
  }

  .carousel-container {
    max-width: 1024px;
    margin: 0 auto;
    padding: 0 2rem;
    padding-bottom: 70px;
  }
</style>
