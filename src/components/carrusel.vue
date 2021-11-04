<template>
  <v-carousel height="400" hide-delimiter-background show-arrows-on-hover>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://www.enviostar.com/wp-content/uploads/2020/12/enviosecommerceivoy.jpg',
          },
          {
            src: 'https://blog.soltekonline.com/content/images/2020/07/1568712199_591499_1568712749_noticia_normal.jpg',
          },
          {
            src: 'https://s3.amazonaws.com/cdn.wp.m4ecmx/wp-content/uploads/2018/05/14054824/Depositphotos_184421302_m-2015-compressor.jpg',
          },
          {
            src: 'https://custodiodedocumentosmx.com/wp-content/uploads/2019/08/Mensajer%C3%ADa-de-documentos-Tu-empresa-lo-necesita-e1567178935565.png',
          },
        ],
      }
    },
  }
</script>