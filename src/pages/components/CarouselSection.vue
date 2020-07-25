<template>
  <div class="section" id="carousel">
    <div class="container">
        <h2 class="title">Our Gallery</h2>
      <div class="row justify-content-center">
        <div class="col-8">
          <el-carousel height="500px">
            <el-carousel-item>
              <img class="d-block" src="img/pic/IMG_0173.jpg" alt="First slide" />
              
            </el-carousel-item>
            <el-carousel-item>
              <img class="d-block" src="img/pic/IMG_0176.jpg" alt="Second slide" />
              <div class="carousel-caption d-none d-md-block">
              </div>
            </el-carousel-item>
            <el-carousel-item>
              <img class="d-block" src="img/pic/IMG_0177.jpg" alt="Third slide" />
              <div class="carousel-caption d-none d-md-block">
              </div>
            </el-carousel-item>
            <el-carousel-item>
              <img class="d-block" src="img/pic/IMG_0178.jpg" alt="4th slide" />
              <div class="carousel-caption d-none d-md-block">
              </div>
            </el-carousel-item>
            <el-carousel-item>
              <img class="d-block" src="img/pic/IMG_0193.jpg" alt="5th slide" />
              <div class="carousel-caption d-none d-md-block">
              </div>
            </el-carousel-item>
            <el-carousel-item>
              <img class="d-block" src="img/pic/IMG_0194.jpg" alt="Third slide" />
              <div class="carousel-caption d-none d-md-block">
              </div>
            </el-carousel-item>
          </el-carousel>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { Carousel, CarouselItem } from 'element-ui';

export default {
  components: {
    [Carousel.name]: Carousel,
    [CarouselItem.name]: CarouselItem
  }
};
</script>
<style></style>
