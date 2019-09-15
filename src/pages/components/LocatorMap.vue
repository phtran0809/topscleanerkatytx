<template>
    <iframe 
        src="https://www.google.com/maps/embed?pb=!1m23!1m12!1m3!1d3464.142803011188!2d-95.77128358460561!3d29.74458003962989!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m8!3e2!4m0!4m5!1s0x864120d77fb73705%3A0x788d47b5b4159b7!2s23106%20Cinco%20Ranch%20Blvd%2C%20Katy%2C%20TX%2077494!3m2!1d29.7445754!2d-95.7690949!5e0!3m2!1sen!2sus!4v1566613778194!5m2!1sen!2sus" 
        width="100%" 
        height="450" 
        frameborder="0" 
        style="border:0;" 
        allowfullscreen="">
    </iframe>
</template>
<script>
export default {
  name: 'LocatorMap',
  data() {
      return {
          center: {lat:29.748393, lng:-95.769422},
          markers:[
              {
                  position:{lat:29.748393, lng:-95.769422}
              }
          ]
      }
  }
}