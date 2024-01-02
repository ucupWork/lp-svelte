<script>
import {Swiper, SwiperSlide} from 'swiper/svelte';
import {FreeMode, Pagination, Autoplay} from 'swiper';
import 'swiper/css';
import 'swiper/css/pagination';

// image source
import proWhey from '../../assets/product/pro-whey.png'
import proIso from '../../assets/product/pro-isolate.png'
import proCasein from '../../assets/product/pro-casein.png'
import proBcaa from '../../assets/product/pro-bcaa.png'
import proCollafit from '../../assets/product/pro-collafit.png'
import proGainer from '../../assets/product/pro-gainer.png'
import proCreatine from '../../assets/product/pro-creatine.png'
import proNrgy from '../../assets/product/pro-nrgy.png'

// product data
let productList = [
  { src: proWhey, name: 'Pro Whey', price: '99.000'},
  { src: proIso, name: 'Pro Isolate', price: '483.750'},
  { src: proCasein, name: 'Pro Casein', price: '371.250'},
  { src: proBcaa, name: 'Pro BCAA', price: '337.500'},
  { src: proCollafit, name: 'Pro Collafit', price: '107.991'},
  { src: proGainer, name: 'Pro Gainer', price: '275.715'},
  { src: proCreatine, name: 'Pro Creatine', price: '226.800'},
  { src: proNrgy, name: 'Pro NRGY', price: '107.991'},
]

</script>

<div class="p-7">
  <h1 class="pl-4 text-2xl font-extrabold text-neutral-600">
    Produk Muscle First
  </h1>
    <Swiper
    spaceBetween={10}
    slidesPerView="auto"
    breakpoints={{
      0: {
        slidesPerView: 1,
        spaceBetween: 10,
      },
      480: {
        slidesPerView: 2,
        spaceBetween: 10,
      },
      768: {
        slidesPerView: 3,
        spaceBetween: 10,
      },
      1024: {
        slidesPerView: 4,
        spaceBetween: 0,
      },
    }}
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
{#each productList as {src, name, price}}
    <SwiperSlide class='p-4'>
              <div class="border rounded-lg m-h-64 p-2 transform hover:translate-y-2 hover:shadow-2xl transition duration-300">
                <figure class="mb-2">
                  <img src={src} alt={`${name} | Muscle first products`} class="border rounded-lg ml-auto mr-auto" />
                </figure>
                <div class="rounded-lg p-4 bg-gray-600 flex flex-col">
                  <div>
                    <h5 class="text-white text-2xl font-bold leading-none">
                      {name}
                    </h5>
                  </div>
                  <div class="flex items-center">
                    <div class="text-lg text-white font-light">
                      Rp.{price}
                    </div>
                    <button href="javascript:;" class="rounded-full bg-gray-800 text-white hover:bg-white hover:text-black hover:shadow-xl focus:outline-none w-10 h-10 flex ml-auto transition duration-300">
                      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="stroke-current m-auto">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 0 0-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 0 0-16.536-1.84M7.5 14.25 5.106 5.272M6 20.25a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Zm12.75 0a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Z" />
                      </svg>
                    </button>
                  </div>
                </div>
              </div>
    </SwiperSlide>
{/each}   

   </Swiper>
</div>
