<template>
  <div>
    <div class="page-header page-header-small">
      <parallax class="page-header-image" style="background-image: url('img/topscleaner.jpg')"></parallax>
      <div class="content-center">
        <div class="container">
          <h1 class="title">Tops Cleaners</h1>
          <h4>
            <a href="tel:(281) 693-6002" style="color:white">
              <i class="fa fa-phone"></i> (281) 693-6002
            </a>
          </h4>
          <h4>
            <a class="nav-link" href="https://goo.gl/maps/PE3PjYJ4xe3oFkz86" target="_blank" style="color:white">
              <i class="now-ui-icons location_map-big"></i> 23106 Cinco Ranch Blvd, Katy, TX 77494
            </a>
          </h4>
          <h4>
            <a class="nav-link" href="#deals" style="color:white">
              <i class="now-ui-icons location_map-big"></i> Current Deals
            </a>
          </h4>
        </div>
      </div>
    </div>
    <div class="section section-about-us">
      <div class="container">
        <div class="row">
          <div class="col-md-8 ml-auto mr-auto text-center">
            <h2 class="title">Who we are?</h2>
            <h5
              class="description"
            >
              Family-owned and operated and committed to excellence in quality and customer service, and we strive to be the best dry cleaners in Katy, TX.
              Our dry cleaning services include fine garment cleaning, executive shirt laundering, clothing repair, clothing alterations, express bag service,
              leather and suede cleaning, comforter cleaning, linen cleaning. We are Eco-Friendly and Use only the finest Green Earth Chemicals.
            
            </h5>
            <h2 class="title">ECO FRIENDLY</h2>
            <h5
              class="description"
              style="text-align:left"
            >
              We are committed to the environment.
              <ul>
                <li>No use of harmful toxic chemicals</li>
                <li>Safe for you and your family</li>
                <li>Safe for the environment</li>
                <li>EPA approved Garments look cleaner, last longer,  feel softer, look brighter and smell fresher</li>
                <li>No allergic reactions</li>
              </ul>
            </h5>
          </div>
        </div>
      </div>
    </div>
    <div class="section section-promotion text-center" id="deals">
      <div class="container">
        <h2 class="title">Current Promotions</h2>
        <div class='promotion'>
          <div class='row'>
             <div class="col-md-12 promotion-card">
              <div class="team-player">
                <h3 class="title">20% OFF</h3>
                <hr>
                <div class="coupon-body">
                  <h3>NEW CUSTOMER DISCOUNT</h3>
                  <p> 20% off Your First Dry Cleaning Order</p>
                  <p><small>*Please mentioned this to our customer service</small></p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <carousel-section></carousel-section>
    <div class="section section-team text-center">
      <div class="container">
        <h2 class="title">Here is our services</h2>
        <div class="team">
          <div class="row">
            <div class="col-md-12">
              <div class="team-player">
                <h4 class="title">Dry Cleaning</h4>
                <h5 class="description"> 
                  Your garments deserve the best care, which is exactly what you'll receive when you take your dry cleaning Tops Cleaners.
                  You can rest assured that we will handle your laundry as if it were our own, using the best possible solution for stain
                   removal and ensuring that every technique used is appropriate for the fabric.
                </h5>
                <div class="price-table">
                  <table class="table">
                    <tbody>
                      <tr v-for="item in dryCleaning">
                        <td class="services-item-name">{{item.item}}</td>
                        <td class="services-item-price">{{item.price}}</td>
                      </tr>
                    </tbody>
                  </table>
                </div>
              </div>
            </div>
            <div class="col-md-12">
              <div class="team-player">
                <h4 class="title">Laundry</h4>
                <h5 class="description"> 
                  You can feel confident each time you put a shirt cleaned by our team! At Tops Cleaners we have taken shirt laundering to a 
                  higher level with care precision and meticulous attention to detail. Each shirt is inspected prior to laundering and 
                  processed based on the fabric type and construction. Stains are pre-treated and the shirts are gently laundered. Our final
                  inspection consists of pressing and hand ironing leaving the shirt looking sharp and as good as new.
                </h5>
                <div class="price-table">
                  <table class="table">
                    <tbody>
                      <tr v-for="item in laudry">
                        <td class="services-item-name">{{item.item}}</td>
                        <td class="services-item-price">{{item.price}}</td>
                      </tr>
                    </tbody>
                  </table>
                  <p>
                    Drop-off and pick-up your
                    <strong>leather items</strong> within
                    <strong>10 business days!</strong> Starting at
                    <strong>$40.00 per garment</strong>; smaller items may be less!
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="section section-team text-center" id="info">
      <div class="container">
        <div class="row">
          <div class="col-md-6" id="location">
            <h2 class="title">We are locate at</h2>
            <p class="category text-primary">
              <a
                href="https://goo.gl/maps/PE3PjYJ4xe3oFkz86"
                target="_blank"
              >23106 Cinco Ranch Blvd, Katy, TX 77494</a>
            </p>
            <LocatorMap />
          </div>
          <div class="col-md-6" id="hours">
            <h2 class="title">Our Hours</h2>
            <p calss="text-primary" v-for="d in hours">{{d.day}}: {{d.time}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { Button, FormGroupInput } from "@/components";
import LocatorMap from "./components/LocatorMap.vue";
import CarouselSection from './components/CarouselSection';
export default {
  name: "TopsCleaners",
  bodyClass: "landing-page",
  components: {
    [Button.name]: Button,
    [FormGroupInput.name]: FormGroupInput,
    LocatorMap,
    CarouselSection,
  },
  data() {
    return {
      dryCleaning: [
        {
          item: "Pants",
          price: "$3.25 - $3.99"
        },
        {
          item: "Blouses",
          price: "$2.99 - $3.99"
        },
        {
          item: "Sweaters",
          price: "$3.99 and Up"
        },
        {
          item: "Jackets",
          price: "$5.99 and Up"
        },
        {
          item: "Dresses",
          price: "$6.99 and Up"
        },
        {
          item: "Two Pices Suits",
          price: "$9.99 and Up"
        },
        {
          item: "Comforter",
          price: "$20.99 and Up"
        }
      ],
      laudry: [
        {
          item: "Executive Shirts",
          price: "$1.79 - $2.69"
        },
        {
          item: "Pants",
          price: "$3.29 - $3.99"
        }
      ],
      hours: [
        {
          day: "Mon",
          time: "7:00 AM – 7:00 PM",
          isOpen: true,
          open: "7:00 AM",
          close: "7:00 PM"
        },
        {
          day: "Tue",
          time: "7:00 AM – 7:00 PM",
          isOpen: true,
          open: "7:00 AM",
          close: "7:00 PM"
        },
        {
          day: "Wed",
          time: "7:00 AM – 7:00 PM",
          isOpen: true,
          open: "7:00 AM",
          close: "7:00 PM"
        },
        {
          day: "Thu",
          time: "7:00 AM – 7:00 PM",
          isOpen: true,
          open: "7:00 AM",
          close: "7:00 PM"
        },
        {
          day: "Fri",
          time: "7:00 AM – 7:00 PM",
          isOpen: true,
          open: "7:00 AM",
          close: "7:00 PM"
        },
        {
          day: "Sat",
          time: "8:00 AM – 5:00 PM",
          isOpen: true,
          open: "8:00 AM",
          close: "5:00 PM"
        },
        {
          day: "Sun",
          isOpen: false,
          time: "Closed"
        }
      ]
    };
  },
  methods: {
    getCurrentStat() {
      var moment = require("moment");
      var day = moment().day() + 2;
      var currentConfig = this.hours[day - 1];
      var nextConfig = this.hours[(day + 6) % 7];
      return nextConfig.day;
      // if(!currentConfig.isOpen){
      //   return ''
      // }
    }
  }
};
</script>
<style></style>
