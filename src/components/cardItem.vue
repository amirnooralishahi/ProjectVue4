<template>
  <div class="Card d-flex border justify-content-center">
    <div class="Card-contain d-flex flex-column">
      <div class="filter-item d-flex gap-4 justify-content-end me-3">
        <p>پربازدید ترین</p>
        <p>حدیدترین</p>
        <p>پرفروش ترین</p>
        <p>گران ترین</p>
        <p>ارزان ترین</p>
      </div>
      <div class="carItems d-flex justify-content-center gap-5 mt-3">
        <div class="cardItem border rounded-4">
          <div class="image" v-for="(item, index) in arrimage" :key="index">
            <img alt="" :src="'${{ item }}'" class="img-fluid" />
          </div>

          <div class="sticker mt-2 p-3 d-flex justify-content-between">
            <div class="logo">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                fill="currentColor"
                class="bi bi-heart"
                viewBox="0 0 16 16"
              >
                <path
                  d="m8 2.748-.717-.737C5.6.281 2.514.878 1.4 3.053c-.523 1.023-.641 2.5.314 4.385.92 1.815 2.834 3.989 6.286 6.357 3.452-2.368 5.365-4.542 6.286-6.357.955-1.886.838-3.362.314-4.385C13.486.878 10.4.28 8.717 2.01zM8 15C-7.333 4.868 3.279-3.04 7.824 1.143q.09.083.176.171a3 3 0 0 1 .176-.17C12.72-3.042 23.333 4.867 8 15"
                />
              </svg>
            </div>
            <div class="text d-flex flex-column gap-1">
              <h3 class="fs-5 overflow-hidden text-end">استیکر</h3>
              <p>قابل چاپ با اندازه دلخواه</p>
            </div>
          </div>
          <div class="price d-flex gap-2 p-3">
            <span class="fw-bold">تومان</span>

            <span class="fw-bold">100,000</span>
          </div>
        </div>
      </div>
    </div>
    <div class="filter border rounded-3 ms-3">
      <div
        class="filter-contain d-flex flex-column align-items-center gap-3 p-3"
      >
        <div class="title d-flex justify-content-between w-100 p-2">
          <span class="delete text-danger fw-bold">حذف فیلتر ها </span>
          <span class="">فیلتر ها </span>
        </div>
        <div class="design d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="text-end w-75 text-secondary">نوع طرح</span>
          </div>
          <div class="line"></div>
        </div>
        <div class="distance d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="text-end w-75 text-secondary">اندازه</span>
          </div>
          <div class="line"></div>
        </div>
        <div class="color d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="text-end w-75 text-secondary">رنگ</span>
          </div>
          <div class="line"></div>
        </div>
        <div class="delivary d-flex flex-column align-items-center w-100">
          <div class="up w-100">
            <div class="icon d-flex w-100 justify-content-between px-4">
              <div
                class="form-check w-100 form-switch d-flex justify-content-between"
              >
                <input
                  class="form-check-input border border-danger"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckDefault"
                />
                <label
                  class="form-check-label text-secondary"
                  for="flexSwitchCheckDefault"
                  >ارسال امروز</label
                >
              </div>
            </div>
          </div>
          <div class="line"></div>
        </div>
        <div class="available d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon d-flex w-100 px-4">
              <div
                class="form-check form-switch w-100 d-flex justify-content-between"
              >
                <input
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckDefault"
                />
                <label
                  class="form-check-label text-secondary"
                  for="flexSwitchCheckDefault"
                  >فقط کالا های موجود</label
                >
              </div>
            </div>
          </div>
          <div class="line"></div>
        </div>

        <div class="graphic d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon d-flex w-100 px-4">
              <div
                class="form-check form-switch w-100 d-flex justify-content-between"
              >
                <input
                  class="form-check-input"
                  type="checkbox"
                  role="switch"
                  id="flexSwitchCheckDefault"
                />
                <label
                  class="form-check-label text-secondary"
                  for="flexSwitchCheckDefault"
                  >فقط محصولات گرافیکی</label
                >
              </div>
            </div>
          </div>
          <div class="line"></div>
        </div>
        <div class="price d-flex flex-column align-items-center w-100">
          <div class="up d-flex w-100 justify-content-center">
            <div class="icon d-flex justify-content-center border">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                fill="currentColor"
                class="bi bi-caret-down-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M7.247 11.14 2.451 5.658C1.885 5.013 2.345 4 3.204 4h9.592a1 1 0 0 1 .753 1.659l-4.796 5.48a1 1 0 0 1-1.506 0z"
                />
              </svg>
            </div>
            <span class="text-end w-75 text-secondary">محدوده قیمت</span>
          </div>
          <div class="line"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const arrimage = ref([
  "../assets/image/9.jpg",
  "../../src/assets/image/2.jpg",
  "../../src/assets/image/3.jpg",
]);
</script>

<style>
</style>