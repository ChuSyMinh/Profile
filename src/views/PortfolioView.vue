<script>
export default {
  data() {
    return {
      activeTab: 1,
      items: [
        {
          id: 1,
          name: 'Phần mềm quản lý sinh viên ',
          imageUrl: 'img/student-management.jpg',
          status: 'Phần mềm quản lý sinh viên hỗ trợ CRUD thông tin sinh viên, điểm thi, giấy tờ nhập học, quan hệ gia đình và giáo viên, hỗ trợ báo cáo theo từng lớp ',
          tech: 'Python, Django, My SQL',
          github: 'https://github.com/ChuSyMinh/student-management-software',
          demo: 'null'
        },
        {
          id: 2,
          name: 'Quản lý Công ty May Quang Nguyệt',
          imageUrl: 'img/company.jpg', 
          status: 'Thiết kế và phát triển phần mềm quản lý nhân sự, tồn kho, báo cáo tài chính, tính lương tự động dựa trên số lượng công đoạn nhân viên đã làm trong một sản phẩm',
          tech: 'Winform, SQL Server, Brevo',
          github: '',
          demo: 'null'
        },
        {
          id: 3,
          name: 'Quản lý nhân viên tại Quang Nguyệt',
          imageUrl: 'img/user.jpg',
          status: 'Xây dựng hệ thống quản lý nhân viên làm việc từ xa, cho phép nhân viên ghi nhận task và cập nhật tiến độ trực tuyến, hỗ trợ nhà quản lý theo dõi và quản lý công việc từ xa ',
          tech: 'ASP .NET , SQL Server , Microservice',
          github: '',
          demo: 'null'
        },
        {
          id: 4,
          name: 'Galaxy',
          imageUrl: 'img/galaxy.png',
          status: 'Giao diện website hiệu ứng không gian vũ trụ, bằng những hình ảnh yêu thích ',
          tech: 'HTML, CSS, JavaScript',
          github: 'https://github.com/ChuSyMinh/galaxy',
          demo: 'https://chusyminh.github.io/galaxy/'
        },
        {
          id: 5,
          name: 'Heart',
          imageUrl: 'img/heart.png', 
          status: 'Hiệu ứng trái tim với những ảnh bản thân',
          tech: 'HTML, CSS, JavaScript',
          github: 'https://github.com/ChuSyMinh/heart',
          demo: 'https://chusyminh.github.io/heart/'
        },
        {
          id: 6,
          name: 'Happy New Year',
          imageUrl: 'img/l.jpg', 
          status: 'Chúc mừng năm mới với hiệu ứng pháo hoa',
          tech: 'HTML, CSS, JavaScript',
          github: 'https://github.com/ChuSyMinh/heart',
          demo: 'https://chusyminh.github.io/HappyNewYear/'
        },
         {
          id: 7,
          name: 'Hands-Free Gaming Controller ',
          imageUrl: 'img/talking tom run.png',
          status: 'chơi game không cần dùng tay bằng cách di chuyển cơ thể ',
          tech: 'Python, OpenCV, Mediapepe',
          github: 'https://github.com/ChuSyMinh/Hands-Free-Gaming-Controller',
          demo: 'null'
        }
      ]
    };
  }
}
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Past Project Experience</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300">
            Explore the projects I've worked on so far</h4>
        </div>
      </header>
      <section>
        <div>
          <div class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
            <div v-for="item in items" :key="item.id">
              <div
                class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5 ">
                <div class="flex h-12 w-12 items-center justify-center p-0 h-full w-full lg:p-0 zoom-in">
                  <img
                    alt="Project image"
                    loading="lazy"
                    decoding="async"
                    data-nimg="1"
                    class="drop-shadow-xl rounded rounded-xl"
                    :src="item.imageUrl" 
                  />
                </div>
                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">{{ item.name }}</div>
                  <div class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-amber-200">
                    {{ item.tech }}
                  </div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                      <a v-if="item.github !== 'null'"
                        :href="item.github" target="_blank" rel="noreferrer"
                        title="View github repository" class="transition-all hover:text-accent">
                        <svg stroke="currentColor"
                          fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"
                          height="16" width="16" xmlns="http://www.w3.org/2000/svg">
                          <path
                            d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22">
                          </path>
                        </svg>
                      </a>
                      <a v-if="item.demo !== 'null'" :href="item.demo" target="_blank" rel="noreferrer"
                        title="View finished project" class="transition-all hover:text-accent">
                        <svg stroke="currentColor"
                          fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"
                          height="18" width="18" xmlns="http://www.w3.org/2000/svg">
                          <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                          <polyline points="15 3 21 3 21 9"></polyline>
                          <line x1="10" y1="14" x2="21" y2="3"></line>
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}
svg:hover {
  stroke: #ffdb70;
}
@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

/* Menggunakan animasi pada elemen yang diinginkan */
.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}
</style>
