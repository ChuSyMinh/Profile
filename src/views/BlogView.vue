<template>
  <div class="container mx-auto p-3 md:p-8">
    <div class="flex flex-col-reverse md:flex-row relative">
      <!-- Danh sách công ty -->
      <div class="w-full md:w-2/3">
        <div class="flex flex-col gap-6 md:px-20 fade-zoom-up">
          <article v-for="article in articles" :key="article.id">
            <a :href="article.url" target="_blank"
              class="block w-full bg-[#1e1e1f] border-[#383838] rounded-xl text-white p-5 md:p-8 hover:bg-[#282828]">
              <!-- Date -->
              <div class="text-xs mb-2 text-slate-400 italic flex items-center">
                <div class="h-[1px] w-20 bg-amber-200 mr-2"></div> {{ article.date }}
              </div>

              <!-- Image -->
              <div class="mb-4">
                <img :src="article.image" alt="" class="w-full h-48 md:h-60 object-cover rounded-xl shadow" />
              </div>

              <!-- Title -->
              <h2 class="text-lg md:text-xl font-bold text-amber-200 mb-2">{{ article.title }}</h2>

              <!-- Description -->
              <p class="text-sm md:text-base text-slate-200 paraf">{{ article.desc }}</p>
            </a>
          </article>
        </div>
      </div>

      <!-- Phần giới thiệu bên phải -->
      <div class="w-full md:w-1/3 h-fit p-8 md:sticky md:top-24">
        <div class="flex flex-col text-left">
          <div class="bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300 text-transparent">
            Các công ty tôi đã từng làm việc, cùng với vai trò và dự án tiêu biểu tại mỗi nơi.
          </div>
          <div class="h-[1px] mt-7 mb-7 w-20 bg-amber-200"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          id: 1,
          title: "Công Ty May Xuất Khẩu Quang Nguyệt",
          date: "01/2021 - Present",
          desc: "Quản lý nhân sự, sản xuất, lập kế hoạch chi phí. Phát triển phần mềm nội bộ giúp giảm 40% thời gian xử lý đơn hàng và tăng độ chính xác tồn kho lên 95%.",
          image: "img/xuong-may-quy-mo-lon.webp",
          url: ""
        },
        {
          id: 2,
          title: "Moi Thue",
          date: "07/2025 - Present",
          desc: "Công việc freelancer, cho thuê trọ trong địa bàn Hà Nội",
          image: "img/Screenshot 2025-07-03 153655.png",
          url: "https://moithue.com/"
        },
        {
          id: 3,
          title: "PNG SOFT",
          date: "12/2024 - 06/2025",
          desc: "Phát triển backend cho hệ thống TMS & B2B. Làm việc trực tiếp với khách hàng và triển khai giải pháp hiệu quả, giúp tăng 30% độ hài lòng và giảm lỗi hệ thống.",
          image: "img/about.jpg.webp",
          url: "https://www.pngsoft.com/"
        }
      ]
    }
  }
}
</script>

<style scoped>
.paraf {
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  text-overflow: ellipsis;
  overflow: hidden;
}
@media (min-width: 768px) {
  .paraf {
    display: -webkit-box;
  }
}
@keyframes fadeZoomUp {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
.fade-zoom-up {
  animation: fadeZoomUp 1s ease-in-out;
}
</style>
