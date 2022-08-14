<template>
  <main class="page__main">
    <div class="container container_main">
      <aside class="main__form aside__form">
        <form class="form-group">
          <div class="input__control">
            <label for="input_success" class="form-group__label">
              <span class="label__text"> Наименование товара </span>
              <div class="form-group__icon">
                <svg width="4" height="4" viewBox="0 0 4 4" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect width="4" height="4" rx="2" fill="#FF8484" />
                </svg>
              </div>
            </label>
            <div class="form-group__input">
              <input
                class="form-group__control"
                type="text"
                id="input_success"
                placeholder="Введите наименование товара"
                value="Success"
              />
            </div>
          </div>
          <div class="input__control">
            <label for="input_success" class="form-group__label">
              <span class="label__text"> Описание товара </span>
            </label>
            <div class="form-group__input">
              <input
                class="form-group__control"
                type="text"
                id="input_success"
                placeholder="Введите описание товара"
                value="Success"
              />
            </div>
          </div>
          <div class="input__control">
            <label for="input_success" class="form-group__label">
              <span class="label__text"> Ссылка на изображение товара </span>
              <div class="form-group__icon">
                <svg width="4" height="4" viewBox="0 0 4 4" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect width="4" height="4" rx="2" fill="#FF8484" />
                </svg>
              </div>
            </label>
            <div class="form-group__input">
              <input
                class="form-group__control"
                type="text"
                id="input_success"
                placeholder="Введите ссылку"
                value="Success"
              />
            </div>
          </div>
          <div class="input__control">
            <label for="input_success" class="form-group__label">
              <span class="label__text"> Цена товара </span>
              <div class="form-group__icon">
                <svg width="4" height="4" viewBox="0 0 4 4" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect width="4" height="4" rx="2" fill="#FF8484" />
                </svg>
              </div>
            </label>
            <div class="form-group__input">
              <input
                class="form-group__control"
                type="text"
                id="input_success"
                placeholder="Введите цену"
                value="Success"
              />
            </div>
          </div>
          <button class="button " disabled="disabled">Добавить товар</button>
        </form>
      </aside>
      <section class="main__cards">
        <div class="main__card">
          <div class="card__icon_delete">
            <svg
              class="card__icon"
              width="16"
              height="16"
              viewBox="0 0 16 16"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g clip-path="url(#clip0_4_349)">
                <path
                  d="M10.207 5.79688C9.99998 5.79688 9.83224 5.96462 9.83224 6.17158V13.2535C9.83224 13.4604 9.99998 13.6283 10.207 13.6283C10.4139 13.6283 10.5817 13.4604 10.5817 13.2535V6.17158C10.5817 5.96462 10.4139 5.79688 10.207 5.79688Z"
                  fill="white"
                />
                <path
                  d="M5.78544 5.79688C5.57848 5.79688 5.41074 5.96462 5.41074 6.17158V13.2535C5.41074 13.4604 5.57848 13.6283 5.78544 13.6283C5.99241 13.6283 6.16015 13.4604 6.16015 13.2535V6.17158C6.16015 5.96462 5.99241 5.79688 5.78544 5.79688Z"
                  fill="white"
                />
                <path
                  d="M2.56294 4.76335V13.9953C2.56294 14.541 2.76303 15.0534 3.11256 15.4211C3.46048 15.7898 3.94467 15.9991 4.4514 16H11.541C12.0478 15.9991 12.532 15.7898 12.8798 15.4211C13.2293 15.0534 13.4294 14.541 13.4294 13.9953V4.76335C14.1242 4.57893 14.5745 3.90768 14.4815 3.19471C14.3884 2.48189 13.7811 1.94867 13.0622 1.94852H11.1437V1.48014C11.1459 1.08626 10.9902 0.708039 10.7113 0.42979C10.4325 0.151688 10.0537 -0.0031709 9.65982 4.92333e-05H6.33255C5.93867 -0.0031709 5.55986 0.151688 5.28103 0.42979C5.00219 0.708039 4.84646 1.08626 4.84865 1.48014V1.94852H2.93019C2.21122 1.94867 1.60393 2.48189 1.51084 3.19471C1.4179 3.90768 1.86813 4.57893 2.56294 4.76335ZM11.541 15.2506H4.4514C3.81075 15.2506 3.31236 14.7002 3.31236 13.9953V4.79629H12.68V13.9953C12.68 14.7002 12.1816 15.2506 11.541 15.2506ZM5.59806 1.48014C5.59558 1.28503 5.67227 1.09724 5.81074 0.959502C5.94906 0.821768 6.13729 0.746095 6.33255 0.749461H9.65982C9.85508 0.746095 10.0433 0.821768 10.1816 0.959502C10.3201 1.09709 10.3968 1.28503 10.3943 1.48014V1.94852H5.59806V1.48014ZM2.93019 2.69793H13.0622C13.4347 2.69793 13.7367 2.99989 13.7367 3.3724C13.7367 3.74491 13.4347 4.04688 13.0622 4.04688H2.93019C2.55768 4.04688 2.25571 3.74491 2.25571 3.3724C2.25571 2.99989 2.55768 2.69793 2.93019 2.69793Z"
                  fill="white"
                />
                <path
                  d="M7.9962 5.79688C7.78923 5.79688 7.62149 5.96462 7.62149 6.17158V13.2535C7.62149 13.4604 7.78923 13.6283 7.9962 13.6283C8.20317 13.6283 8.37091 13.4604 8.37091 13.2535V6.17158C8.37091 5.96462 8.20317 5.79688 7.9962 5.79688Z"
                  fill="white"
                />
              </g>
              <defs>
                <clipPath id="clip0_4_349">
                  <rect width="16" height="16" fill="white" />
                </clipPath>
              </defs>
            </svg>
          </div>
          <div class="card__wrapper-img">
            <img class="card__img" src="@/assets/logo.png" alt="#" srcset="" />
          </div>
          <div class="card__content">
            <div class="card__header">Наименование товара</div>
            <div class="card__info">
              Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в
              несколько строк
            </div>
            <div class="card__price">10 000 руб.</div>
          </div>
        </div>
        <div class="main__card">
          <div class="card__icon_delete">
            <svg
              class="card__icon"
              width="16"
              height="16"
              viewBox="0 0 16 16"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g clip-path="url(#clip0_4_349)">
                <path
                  d="M10.207 5.79688C9.99998 5.79688 9.83224 5.96462 9.83224 6.17158V13.2535C9.83224 13.4604 9.99998 13.6283 10.207 13.6283C10.4139 13.6283 10.5817 13.4604 10.5817 13.2535V6.17158C10.5817 5.96462 10.4139 5.79688 10.207 5.79688Z"
                  fill="white"
                />
                <path
                  d="M5.78544 5.79688C5.57848 5.79688 5.41074 5.96462 5.41074 6.17158V13.2535C5.41074 13.4604 5.57848 13.6283 5.78544 13.6283C5.99241 13.6283 6.16015 13.4604 6.16015 13.2535V6.17158C6.16015 5.96462 5.99241 5.79688 5.78544 5.79688Z"
                  fill="white"
                />
                <path
                  d="M2.56294 4.76335V13.9953C2.56294 14.541 2.76303 15.0534 3.11256 15.4211C3.46048 15.7898 3.94467 15.9991 4.4514 16H11.541C12.0478 15.9991 12.532 15.7898 12.8798 15.4211C13.2293 15.0534 13.4294 14.541 13.4294 13.9953V4.76335C14.1242 4.57893 14.5745 3.90768 14.4815 3.19471C14.3884 2.48189 13.7811 1.94867 13.0622 1.94852H11.1437V1.48014C11.1459 1.08626 10.9902 0.708039 10.7113 0.42979C10.4325 0.151688 10.0537 -0.0031709 9.65982 4.92333e-05H6.33255C5.93867 -0.0031709 5.55986 0.151688 5.28103 0.42979C5.00219 0.708039 4.84646 1.08626 4.84865 1.48014V1.94852H2.93019C2.21122 1.94867 1.60393 2.48189 1.51084 3.19471C1.4179 3.90768 1.86813 4.57893 2.56294 4.76335ZM11.541 15.2506H4.4514C3.81075 15.2506 3.31236 14.7002 3.31236 13.9953V4.79629H12.68V13.9953C12.68 14.7002 12.1816 15.2506 11.541 15.2506ZM5.59806 1.48014C5.59558 1.28503 5.67227 1.09724 5.81074 0.959502C5.94906 0.821768 6.13729 0.746095 6.33255 0.749461H9.65982C9.85508 0.746095 10.0433 0.821768 10.1816 0.959502C10.3201 1.09709 10.3968 1.28503 10.3943 1.48014V1.94852H5.59806V1.48014ZM2.93019 2.69793H13.0622C13.4347 2.69793 13.7367 2.99989 13.7367 3.3724C13.7367 3.74491 13.4347 4.04688 13.0622 4.04688H2.93019C2.55768 4.04688 2.25571 3.74491 2.25571 3.3724C2.25571 2.99989 2.55768 2.69793 2.93019 2.69793Z"
                  fill="white"
                />
                <path
                  d="M7.9962 5.79688C7.78923 5.79688 7.62149 5.96462 7.62149 6.17158V13.2535C7.62149 13.4604 7.78923 13.6283 7.9962 13.6283C8.20317 13.6283 8.37091 13.4604 8.37091 13.2535V6.17158C8.37091 5.96462 8.20317 5.79688 7.9962 5.79688Z"
                  fill="white"
                />
              </g>
              <defs>
                <clipPath id="clip0_4_349">
                  <rect width="16" height="16" fill="white" />
                </clipPath>
              </defs>
            </svg>
          </div>
          <div class="card__wrapper-img">
            <img class="card__img" src="@/assets/logo.png" alt="#" srcset="" />
          </div>
          <div class="card__content">
            <div class="card__header">Наименование товара</div>
            <div class="card__info">
              Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в
              несколько строк
            </div>
            <div class="card__price">10 000 руб.</div>
          </div>
        </div>
        <div class="main__card">
          <div class="card__icon_delete">
            <svg
              class="card__icon"
              width="16"
              height="16"
              viewBox="0 0 16 16"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <g clip-path="url(#clip0_4_349)">
                <path
                  d="M10.207 5.79688C9.99998 5.79688 9.83224 5.96462 9.83224 6.17158V13.2535C9.83224 13.4604 9.99998 13.6283 10.207 13.6283C10.4139 13.6283 10.5817 13.4604 10.5817 13.2535V6.17158C10.5817 5.96462 10.4139 5.79688 10.207 5.79688Z"
                  fill="white"
                />
                <path
                  d="M5.78544 5.79688C5.57848 5.79688 5.41074 5.96462 5.41074 6.17158V13.2535C5.41074 13.4604 5.57848 13.6283 5.78544 13.6283C5.99241 13.6283 6.16015 13.4604 6.16015 13.2535V6.17158C6.16015 5.96462 5.99241 5.79688 5.78544 5.79688Z"
                  fill="white"
                />
                <path
                  d="M2.56294 4.76335V13.9953C2.56294 14.541 2.76303 15.0534 3.11256 15.4211C3.46048 15.7898 3.94467 15.9991 4.4514 16H11.541C12.0478 15.9991 12.532 15.7898 12.8798 15.4211C13.2293 15.0534 13.4294 14.541 13.4294 13.9953V4.76335C14.1242 4.57893 14.5745 3.90768 14.4815 3.19471C14.3884 2.48189 13.7811 1.94867 13.0622 1.94852H11.1437V1.48014C11.1459 1.08626 10.9902 0.708039 10.7113 0.42979C10.4325 0.151688 10.0537 -0.0031709 9.65982 4.92333e-05H6.33255C5.93867 -0.0031709 5.55986 0.151688 5.28103 0.42979C5.00219 0.708039 4.84646 1.08626 4.84865 1.48014V1.94852H2.93019C2.21122 1.94867 1.60393 2.48189 1.51084 3.19471C1.4179 3.90768 1.86813 4.57893 2.56294 4.76335ZM11.541 15.2506H4.4514C3.81075 15.2506 3.31236 14.7002 3.31236 13.9953V4.79629H12.68V13.9953C12.68 14.7002 12.1816 15.2506 11.541 15.2506ZM5.59806 1.48014C5.59558 1.28503 5.67227 1.09724 5.81074 0.959502C5.94906 0.821768 6.13729 0.746095 6.33255 0.749461H9.65982C9.85508 0.746095 10.0433 0.821768 10.1816 0.959502C10.3201 1.09709 10.3968 1.28503 10.3943 1.48014V1.94852H5.59806V1.48014ZM2.93019 2.69793H13.0622C13.4347 2.69793 13.7367 2.99989 13.7367 3.3724C13.7367 3.74491 13.4347 4.04688 13.0622 4.04688H2.93019C2.55768 4.04688 2.25571 3.74491 2.25571 3.3724C2.25571 2.99989 2.55768 2.69793 2.93019 2.69793Z"
                  fill="white"
                />
                <path
                  d="M7.9962 5.79688C7.78923 5.79688 7.62149 5.96462 7.62149 6.17158V13.2535C7.62149 13.4604 7.78923 13.6283 7.9962 13.6283C8.20317 13.6283 8.37091 13.4604 8.37091 13.2535V6.17158C8.37091 5.96462 8.20317 5.79688 7.9962 5.79688Z"
                  fill="white"
                />
              </g>
              <defs>
                <clipPath id="clip0_4_349">
                  <rect width="16" height="16" fill="white" />
                </clipPath>
              </defs>
            </svg>
          </div>
          <div class="card__wrapper-img">
            <img class="card__img" src="@/assets/logo.png" alt="#" srcset="" />
          </div>
          <div class="card__content">
            <div class="card__header">Наименование товара</div>
            <div class="card__info">
              Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в
              несколько строк
            </div>
            <div class="card__price">10 000 руб.</div>
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<script>
export default {
  name: 'pageMain',
};
</script>

<style lang="sass">


.page__main
    padding-top: 1rem

.container_main
    display: grid
    grid-template-columns: 332px 1fr

.container 
  max-width: 1376px;
  margin: 0 auto;


.main__form
    padding: 1.5rem
    background: var(--white)
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02)
    border-radius: 4px

.form-group
    /* width: 100%; */
    display: grid
    grid-template-columns: 1fr
    gap: 1rem


    &__label

        font-style: normal
        font-weight: 400
        font-size: 10px
        line-height: 13px
        letter-spacing: -0.02em

        color: var(--darkfiol)
        position: relative


    &__icon
        display: inline
        width: 4px
        height: 4px
        position: absolute


    &__input
        display: inline-flex


    &__input .form-group__control
        background: var(--white)
        box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1)
        border-radius: 4px

        font-family: 'Inter'
        font-style: normal
        font-weight: 400
        font-size: 20px
        line-height: 26px
        padding-top: 10px
        padding-left: 16px
        padding-bottom: 11px

        width: 100%
        outline: none
        border: none

// /* .form-group .form-group__input .form-group__control:focus {
//  border: 1px solid var(--blue-3);
//  box-shadow: 0px 1px 1px rgba(51, 154, 240, 0.1);


//     &_success .form-group__input .form-group__control:focus
//         border: 1px solid var(--blue-3)
//         box-shadow: 0px 1px 1px rgba(51, 154, 240, 0.1)


//     &_invalid .form-group__input .form-group__control:focus
//         border: 1px solid var(--red)
//         box-shadow: 0px 1px 1px rgba(240, 61, 62, 0.1)
//         border-radius: 8px
// } */

/* button block */

.button
    height: 36px
    border-radius: 10px
    font-family: 'Inter'
    font-style: normal
    font-weight: 600
    font-size: 12px
    line-height: 15px
    text-align: center
    /* transition: opacity 200ms ease-in-out, background 200ms ease-in-out; */
    padding: 10px 95px 11px 95px
    border: none
    cursor: pointer
    display: inline-block
    white-space: nowrap;
    background: #7BAE73
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1)
    border-radius: 10px


    &:disabled
        color: #B4B4B4
        background: var(--white-disable)
        pointer-events: none
        box-shadow: none

// /* primary block


//     &_primary
//         background-color: var(--primary-background-color)
//         color: var(--primary-color)


//     &_primary:hover
//         background-color: var(--primary-hover)

// /* secondary block */

// /* .button_secondary {
//  background-color: var(--secondary-background-color);
//  color: var(--secondary-color);


//     &_secondary:hover
//         background-color: var(--secondary-hover)

// /* alternate block */

// /* .button_alternate {
//  background-color: var(--alternate-background-color);
//  color: var(--alternate-color);
//  box-sizing: border-box;
//  border: 1px solid #ACB5BD;


//     &_alternate:hover
//         border: 1px solid #212429
// }  */

.main__cards
    display: grid
    /* grid-template-columns: repeat(auto-fill, minmax(332px, 1fr));
     */
    grid-template-columns: repeat(3, 320px)
    gap: 16px

.main__card
    display: grid
    grid-template-columns: 1fr
    position: relative
    gap: 16px

.card__icon_delete
    display: inline
    width: 16px
    height: 16px
    top: -8px
    right: -9.5px
    padding: 8px 9.5px
    position: absolute

    background: #FF8484
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1)
    border-radius: 10px

.card__wrapper-img
    width: 100%
    height: 200px
    border-radius: 4px 4px 0px 0px

.card__img
    width: 100%
    height: 100%
    object-fit: cover
    // /* border-radius: 50%;
    // border: none; */

.card__content
    display: grid
    grid-template-columns: 1fr
    padding-left: 1rem
    padding-right: 1rem
    padding-bottom: 1.5rem
    /* 16 16 24px */

.card__header
    /* Наименование товара */

    font-family: 'Source Sans Pro'
    font-style: normal
    font-weight: 600
    font-size: 20px
    line-height: 25px
    text-align: start
    color: var(--brown)

.card__info
    word-wrap: break-word

    font-family: 'Source Sans Pro'
    font-style: normal
    font-weight: 400
    font-size: 16px
    line-height: 20px

    color: var(--brown)

.card__price

    font-family: 'Source Sans Pro'
    font-style: normal
    font-weight: 600
    font-size: 24px
    line-height: 30px

    color: var(--brown)
</style>