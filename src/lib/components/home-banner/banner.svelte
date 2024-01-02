<script>
    import {Swiper, SwiperSlide} from 'swiper/svelte';
    import {FreeMode, Pagination, Autoplay} from 'swiper';
    import 'swiper/css';
    import 'swiper/css/pagination';
    
    // image source
    import banner1 from '../../assets/banner/banner2.webp'
    import banner2 from '../../assets/banner/banner1.webp'
    import banner3 from '../../assets/banner/banner3.webp'
    
    </script>
    
    <div class="px-12">
        <Swiper
        slidesPerView="auto"      
        freeMode={true}
        pagination={{
          clickable: true,
        }}
        autoplay={{
          delay: 4000,
          disableOnInteraction: false,
        }}
        loop={true}
        modules={[FreeMode, Pagination,  Autoplay]}
        className="mySwipe"
      >
        <SwiperSlide>
            <img src={banner1} alt="Promo Muscle First" class="w-full h-full rounded-lg">
        </SwiperSlide>
        <SwiperSlide>
            <img src={banner2} alt="Promo Muscle First" class="w-full h-full rounded-lg">
        </SwiperSlide>
        <SwiperSlide>
            <img src={banner3} alt="Promo Muscle First" class="w-full h-full rounded-lg">
        </SwiperSlide>
       </Swiper>
    </div>
    