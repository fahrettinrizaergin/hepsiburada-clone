<template>
  <header>
    <div class="flex flex-col space-y-3">
      <div class="topLinks container">
        <ul class="flex justify-end items-end gap-3 h-7">
          <li v-for="navItem in topNavbar" :key="navItem" class="h-5 text-xs font-semibold">
            <router-link :to="navItem.path">{{ navItem.label }}</router-link>
          </li>
        </ul>
      </div>
      <div class="container flex items-center justify-between">
        <div class="logo w-2/12">
          <router-link to="/" class="text-right max-w-max">
            <svg width="191" height="34" class="-mb-1" viewBox="0 0 171 28" xmlns="http://www.w3.org/2000/svg"><path d="M11.525 6.04c.808.344 1.471.87 1.99 1.58.44.6.71 1.218.807 1.852.099.635.148 1.671.148 3.108v9.448h-4.293v-9.79c0-.866-.146-1.565-.439-2.097-.38-.748-1.103-1.122-2.167-1.122-1.103 0-1.94.371-2.511 1.115-.571.743-.856 1.804-.856 3.182v8.712H0V.08h4.204v7.243c.778-.768 1.167-1.018 1.945-1.327.817-.324 1.8-.473 2.68-.473.99 0 1.888.172 2.696.517zm10.242 3.868c-.594.612-.967 1.442-1.12 2.488h7.242c-.076-1.115-.45-1.962-1.12-2.54-.67-.578-1.5-.867-2.493-.867-1.079 0-1.915.307-2.509.92zm6.289-3.632c1.121.503 2.048 1.296 2.778 2.379.658.955 1.086 2.063 1.281 3.324.113.738.159 1.802.138 3.19h-11.71c.066 1.613.626 2.744 1.682 3.393.642.404 1.415.605 2.318.605.957 0 1.736-.246 2.334-.738.326-.265.615-.634.865-1.106h4.292c-.113.954-.633 1.923-1.558 2.906-1.44 1.563-3.457 2.345-6.049 2.345-2.14 0-4.027-.66-5.663-1.978-1.636-1.32-2.453-3.464-2.453-6.437 0-2.785.738-4.92 2.214-6.407 1.477-1.486 3.393-2.229 5.75-2.229 1.399 0 2.66.251 3.78.753zM44.628 10.7c-.571-.953-1.498-1.43-2.78-1.43-1.54 0-2.597.722-3.173 2.168-.298.767-.447 1.74-.447 2.92 0 1.869.501 3.182 1.504 3.938.596.443 1.301.664 2.116.664 1.182 0 2.084-.452 2.706-1.357.62-.904.93-2.109.93-3.614 0-1.238-.285-2.335-.856-3.289zm3.226-3.024c1.312 1.387 1.967 3.423 1.967 6.107 0 2.832-.64 4.99-1.922 6.475-1.282 1.485-2.932 2.228-4.951 2.228-1.287 0-2.356-.32-3.207-.959-.465-.354-.92-.87-1.366-1.55v7.96h-4.159V5.95h4.027v2.375c.455-.697.94-1.248 1.454-1.652.94-.717 2.059-1.077 3.355-1.077 1.89 0 3.491.694 4.802 2.08zm7.588 9.22c.089.747.281 1.278.578 1.592.523.56 1.492.84 2.905.84.83 0 1.49-.122 1.978-.368.49-.245.734-.614.734-1.106 0-.472-.197-.83-.591-1.077-.394-.245-1.86-.669-4.398-1.268-1.827-.453-3.114-1.017-3.861-1.697-.748-.668-1.121-1.632-1.121-2.89 0-1.485.584-2.761 1.751-3.828 1.168-1.067 2.811-1.6 4.93-1.6 2.01 0 3.649.4 4.915 1.202 1.266.801 1.993 2.185 2.18 4.152h-4.204c-.059-.541-.212-.968-.458-1.284-.464-.57-1.253-.855-2.366-.855-.918 0-1.57.143-1.96.428-.39.285-.584.62-.584 1.003 0 .482.207.83.62 1.047.415.227 1.878.615 4.39 1.165 1.674.394 2.93.988 3.766 1.785.826.807 1.239 1.815 1.239 3.024 0 1.593-.594 2.893-1.781 3.901-1.188 1.008-3.023 1.512-5.506 1.512-2.532 0-4.402-.534-5.608-1.6-1.208-1.067-1.81-2.427-1.81-4.079h4.262zm12.676 5.132V5.951h4.263v16.077h-4.263zm17.888-4.35c.605-.876.908-2.026.908-3.452 0-1.141-.149-2.085-.446-2.833-.565-1.415-1.606-2.123-3.123-2.123-1.537 0-2.593.693-3.168 2.08-.298.737-.446 1.69-.446 2.86 0 1.378.307 2.518.922 3.423.615.905 1.551 1.357 2.81 1.357 1.091 0 1.939-.437 2.543-1.313zm3.514-9.795c1.203 1.524 1.804 3.491 1.804 5.9 0 2.498-.593 4.568-1.78 6.21-1.185 1.642-2.84 2.463-4.966 2.463-1.334 0-2.407-.265-3.217-.796-.484-.315-1.008-.865-1.571-1.652v2.02h-4.145V.036h4.204v8.01c.534-.748 1.123-1.318 1.766-1.712.762-.491 1.732-.737 2.91-.737 2.128 0 3.793.762 4.995 2.286zm8.31-1.932v9.69c0 .915.107 1.604.323 2.066.381.816 1.13 1.224 2.245 1.224 1.428 0 2.407-.58 2.935-1.74.274-.63.412-1.46.412-2.493V5.95h4.262v16.077h-4.086v-2.271a8.17 8.17 0 00-.294.442 2.928 2.928 0 01-.559.65c-.657.59-1.291.993-1.905 1.21-.612.215-1.33.323-2.154.323-2.373 0-3.972-.855-4.795-2.566-.461-.944-.692-2.335-.692-4.174V5.95h4.308zm22.35-.376c.055.005.175.012.362.022v4.307a11.593 11.593 0 00-1.21-.074c-1.691 0-2.826.551-3.407 1.652-.325.62-.486 1.574-.486 2.862v7.684h-4.234V5.951h4.012v2.802c.65-1.071 1.215-1.804 1.696-2.197.787-.659 1.81-.988 3.069-.988.078 0 .145.002.198.007zm28.693 12.087c.62-.885.93-2.03.93-3.436 0-1.967-.497-3.373-1.49-4.219a3.208 3.208 0 00-2.124-.767c-1.23 0-2.131.465-2.707 1.394-.575.93-.863 2.083-.863 3.459 0 1.485.293 2.672.878 3.562.585.89 1.472 1.335 2.662 1.335s2.095-.442 2.714-1.328zM147.841 6.21a5.112 5.112 0 011.844 1.778V.037h4.262v21.991h-4.085v-2.227c-.6.954-1.284 1.648-2.05 2.08-.768.433-1.721.649-2.862.649-1.878 0-3.459-.76-4.742-2.279-1.284-1.52-1.925-3.468-1.925-5.849 0-2.743.632-4.9 1.895-6.474 1.264-1.574 2.953-2.36 5.067-2.36.973 0 1.838.213 2.596.64zm-15.853 8.035c-.268.167-.54.302-.813.404-.274.103-.649.2-1.127.288l-.954.176c-.895.157-1.538.349-1.928.575-.661.382-.991.976-.991 1.78 0 .716.201 1.234.605 1.553.403.32.894.478 1.472.478.917 0 1.761-.264 2.534-.794.772-.53 1.172-1.497 1.202-2.9v-1.56zm.133 7.798s.03-1.518 0-1.881a8.662 8.662 0 01-2.013 1.604c-.908.52-1.935.78-3.08.78-1.46 0-2.667-.414-3.62-1.244-.952-.829-1.428-2.003-1.428-3.524 0-1.973.766-3.4 2.298-4.283.84-.481 2.076-.825 3.707-1.03l1.438-.178c.781-.098 1.34-.22 1.676-.368.602-.255.905-.652.905-1.192 0-.657-.232-1.111-.695-1.361-.462-.25-1.14-.375-2.036-.375-1.005 0-1.716.245-2.133.735-.299.363-.498.854-.597 1.472h-4.048c.089-1.403.483-2.555 1.183-3.46 1.113-1.411 3.025-2.118 5.735-2.118 1.764 0 3.331.349 4.701 1.044 1.37.698 2.054 2.012 2.054 3.945v7.36c0 .51.01 3.348.03 4.074h-4.077zm34.028-7.798a4.53 4.53 0 01-.814.404 6.902 6.902 0 01-1.126.288l-.955.176c-.895.157-1.537.349-1.928.575-.66.382-.991.976-.991 1.78 0 .716.202 1.234.606 1.553.403.32.894.478 1.472.478.916 0 1.76-.264 2.533-.794.772-.53 1.173-1.497 1.203-2.9v-1.56zm.132 7.798s.03-1.518 0-1.881a8.675 8.675 0 01-2.013 1.604c-.908.52-1.935.78-3.08.78-1.46 0-2.667-.414-3.62-1.244-.951-.829-1.427-2.003-1.427-3.524 0-1.973.765-3.4 2.297-4.283.84-.481 2.077-.825 3.707-1.03l1.439-.178c.78-.098 1.339-.22 1.675-.368.603-.255.905-.652.905-1.192 0-.657-.231-1.111-.694-1.361-.463-.25-1.141-.375-2.036-.375-1.005 0-1.717.245-2.134.735-.299.363-.497.854-.597 1.472h-4.048c.089-1.403.483-2.555 1.183-3.46 1.113-1.411 3.025-2.118 5.736-2.118 1.763 0 3.33.349 4.7 1.044 1.37.698 2.055 2.012 2.055 3.945v7.36c0 .51.01 3.348.03 4.074h-4.078zM72.496 2.315a2.315 2.315 0 11-4.629 0 2.315 2.315 0 014.63 0z" fill="#FF6000" fill-rule="evenodd"></path></svg>
            <b class="p-0 m-0 font-bold text-sm w-full text-right">Premium'u ke??fet</b>
          </router-link>
        </div>
        <div class="search w-5/12 pl-14">
          <div class="search-container py-0.5 border-2 border-neutral-400 rounded relative flex">
            <svg x="0px" y="0px" viewBox="0 0 487.95 487.95" class="absolute top-1/2 -translate-y-1/2 w-6 h-6 ml-2 fill-neutral-400"><g><g><path d="M481.8,453l-140-140.1c27.6-33.1,44.2-75.4,44.2-121.6C386,85.9,299.5,0.2,193.1,0.2S0,86,0,191.4s86.5,191.1,192.9,191.1 c45.2,0,86.8-15.5,119.8-41.4l140.5,140.5c8.2,8.2,20.4,8.2,28.6,0C490,473.4,490,461.2,481.8,453z M41,191.4 c0-82.8,68.2-150.1,151.9-150.1s151.9,67.3,151.9,150.1s-68.2,150.1-151.9,150.1S41,274.1,41,191.4z"/></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></svg>
            <input type="text" class="py-2 pl-10 pr-4 outline-0 placehplder:color-neutral-400 w-full" placeholder="asd" />
            <button class="bg-neutral-400 py-2.5 px-3 -my-0.5 text-white font-bold">ARA</button>
          </div>
        </div>
        <div class="location w-2/12 pl-7">
          <div class="flex items-center gap-3 cursor-pointer">
            <svg viewBox="0 0 368.666 368.666" class="w-6 h-7 fill-orange-600"><g id="XMLID_2_"><g><g><path d="M184.333,0C102.01,0,35.036,66.974,35.036,149.297c0,33.969,11.132,65.96,32.193,92.515 c27.27,34.383,106.572,116.021,109.934,119.479l7.169,7.375l7.17-7.374c3.364-3.46,82.69-85.116,109.964-119.51 c21.042-26.534,32.164-58.514,32.164-92.485C333.63,66.974,266.656,0,184.333,0z M285.795,229.355 c-21.956,27.687-80.92,89.278-101.462,110.581c-20.54-21.302-79.483-82.875-101.434-110.552 c-18.228-22.984-27.863-50.677-27.863-80.087C55.036,78.002,113.038,20,184.333,20c71.294,0,129.297,58.002,129.296,129.297 C313.629,178.709,304.004,206.393,285.795,229.355z"/><path d="M184.333,59.265c-48.73,0-88.374,39.644-88.374,88.374c0,48.73,39.645,88.374,88.374,88.374s88.374-39.645,88.374-88.374 S233.063,59.265,184.333,59.265z M184.333,216.013c-37.702,0-68.374-30.673-68.374-68.374c0-37.702,30.673-68.374,68.374-68.374 s68.373,30.673,68.374,68.374C252.707,185.341,222.035,216.013,184.333,216.013z"/></g></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></svg>
            <div class="m-0 p-0">
              <b class="block font-bold -mb-2 -mt-1">Konum</b>
              <div class="flex">
                <b class="block font-normal text-xs -mb-1 text-orange-600">Konum Se??</b>
                <svg viewBox="0 0 25.93 25.93" class="w-2 ml-2 mt-1 fill-orange-600"><g><g id="c118_triangle"><path d="M25.397,4.554h-2.042l-9.974,12.644c-0.101,0.124-0.256,0.197-0.416,0.197c-0.164,0-0.315-0.073-0.419-0.197L2.575,4.554 H0.532c-0.206,0-0.392,0.115-0.479,0.299c-0.09,0.184-0.064,0.403,0.06,0.561l12.435,15.762c0.104,0.125,0.255,0.2,0.419,0.2 c0.16,0,0.315-0.075,0.416-0.2L25.816,5.413c0.128-0.157,0.148-0.377,0.058-0.561C25.789,4.669,25.601,4.554,25.397,4.554z"/></g><g id="Capa_1_184_"></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></svg>
              </div>
            </div>
          </div>
        </div>
        <div class="account w-3/12">
          <div class="flex items-center gap-4">
            <button class="border-2 border-neutral-500 bg-white h-full px-4 h-12 rounded flex items-center gap-2.5">
              <svg viewBox="0 0 96 96" class="w-5 h-7"><path d="M69.3677,51.0059a30,30,0,1,0-42.7354,0A41.9971,41.9971,0,0,0,0,90a5.9966,5.9966,0,0,0,6,6H90a5.9966,5.9966,0,0,0,6-6A41.9971,41.9971,0,0,0,69.3677,51.0059ZM48,12A18,18,0,1,1,30,30,18.02,18.02,0,0,1,48,12ZM12.5977,84A30.0624,30.0624,0,0,1,42,60H54A30.0624,30.0624,0,0,1,83.4023,84Z"/></svg>
              <div>
                <b class="block -mb-1.5 text-sm">Giri?? Yap</b>
                <small class="block text-xxs text-left">veya ??ye ol</small>
              </div>
              <svg viewBox="0 0 25.93 25.93" class="w-3"><g><g id="c118_triangle"><path d="M25.397,4.554h-2.042l-9.974,12.644c-0.101,0.124-0.256,0.197-0.416,0.197c-0.164,0-0.315-0.073-0.419-0.197L2.575,4.554 H0.532c-0.206,0-0.392,0.115-0.479,0.299c-0.09,0.184-0.064,0.403,0.06,0.561l12.435,15.762c0.104,0.125,0.255,0.2,0.419,0.2 c0.16,0,0.315-0.075,0.416-0.2L25.816,5.413c0.128-0.157,0.148-0.377,0.058-0.561C25.789,4.669,25.601,4.554,25.397,4.554z"/></g><g id="Capa_1_184_"></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></svg>
            </button>
            <button class="bg-neutral-400 text-white font-bolder py-3 px-4 h-12 rounded flex gap-3 items-center">
              <svg viewBox="0 0 268.89 268.89" class="w-6"><g><g><path style="fill:#ffffff;" d="M117.696,215.019c-14.804,0-26.851,12.053-26.851,26.851c0,14.804,12.047,26.851,26.851,26.851 s26.851-12.047,26.851-26.851C144.547,227.066,132.506,215.019,117.696,215.019z"/><path style="fill:#ffffff;" d="M201.841,215.019c-14.804,0-26.851,12.053-26.851,26.851c0,14.804,12.047,26.851,26.851,26.851 c14.798,0,26.851-12.047,26.851-26.851C228.692,227.066,216.639,215.019,201.841,215.019z"/><path style="fill:#ffffff;" d="M267.62,68.109c-1.128-1.444-2.858-2.285-4.696-2.285H61.178l-16.63-61.25 c-0.036-0.131-0.131-0.233-0.179-0.358c-0.131-0.388-0.328-0.728-0.537-1.074c-0.197-0.328-0.376-0.65-0.627-0.931 c-0.245-0.28-0.531-0.489-0.829-0.716c-0.31-0.239-0.609-0.471-0.961-0.644c-0.328-0.167-0.68-0.251-1.044-0.358 c-0.388-0.113-0.764-0.209-1.175-0.239c-0.143-0.006-0.263-0.084-0.412-0.084H5.967C2.673,0.17,0,2.843,0,6.137 s2.673,5.967,5.967,5.967H34.22l16.606,61.172l29.822,120.811c0.656,2.667,3.049,4.541,5.794,4.541h146.642 c2.745,0,5.132-1.868,5.794-4.541l29.834-120.865C269.159,71.438,268.754,69.558,267.62,68.109z"/></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></svg>
              <p class="m-0 p-0">Sepetim 3</p>
            </button>
          </div>
        </div>
      </div>
      <div class="flex colorBand">
        <div class="bg-violet-700 p-1 w-full"></div>
        <div class="bg-cyan-400 p-1 w-full"></div>
        <div class="bg-orange-600 p-1 w-full"></div>
        <div class="bg-amber-500 p-1 w-full"></div>
        <div class="bg-fuchsia-800 p-1 w-full"></div>
        <div class="bg-emerald-400 p-1 w-full"></div>
      </div>
    </div>
    <div class="navbar">
      <div class="container">
        <ul class="flex items-center">
          <li class="text-lg" v-for="navItem in navbar" :key="navItem">
            <div class="w-[8.6rem] h-14 flex items-center text-sm leading-5 before:block before:w-0.5 before:h-6 before:bg-neutral-200">
              <div class="w-full px-4 text-center font-semibold">
                {{ navItem.label }}
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponents',
  data () {
    return {
      topNavbar: [
        { label: 'Sipari??lerim', path: '#' },
        { label: 'S??per Fiyat, S??per Teklif', path: '#' },
        { label: 'Yurt D??????ndan', path: '#' },
        { label: 'Kampanyalar', path: '#' },
        { label: 'Giri??imci Kad??nlar', path: '#' },
        { label: '????z??m Merkezi', path: '#' },
        { label: 'Hepsiburada Premium', path: '#' },
        { label: 'Hepsiburada\'da Sat??c?? Ol', path: '#' }
      ],
      navbar: [
        { label: 'Elektronik', path: '#' },
        { label: 'Moda', path: '#' },
        { label: 'Ev, Ya??am, K??rtasiye, Ofis', path: '#' },
        { label: 'Oto, Bah??e, Yap?? Market', path: '#' },
        { label: 'Anne, Bebek, Oyuncak', path: '#' },
        { label: 'Spor, Outdoor', path: '#' },
        { label: 'Kozmetik, Ki??isel Bak??m', path: '#' },
        { label: 'S??permarket, Pet Shop', path: '#' },
        { label: 'Kitap, M??zik, Film, Hobi', path: '#' }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>
