<template>
<!-- service area start here -->
<section class="service-area service-area2 pt-115 pb-100" :style="{backgroundImage: 'url('+require('../../public/assets/img/service/service-bg.jpg') +')'}">
    <div class="container">
        <div class="row justify-content-between">
            <div class="col-xxl-6 col-lg-6">
                <div class="kservice-text mb-50 aos-init aos-animate" data-aos="fade-right" data-aos-duration="1000">
                    <h5 class="kservice-text-subtitle mb-15">{{ sectionSubTitle }}</h5>
                    <h2 class="kservice-text-title mb-40" v-html="sectionTitle">{{ sectionTitle }}</h2>
                </div>
            </div>
            <div class="col-xxl-5 col-lg-6">
                <div class="kservice-text mb-50 aos-init aos-animate" data-aos="fade-right" data-aos-duration="1000">
                    <p class="mb-45 mt-35 mt-md-0 mt-xs-0">{{descripionText}}</p>
                </div>
            </div>
        </div>

        <div class="row custom-mar-20 aos-init aos-animate" data-aos="fade-down" data-aos-duration="1000">
            <div class="col-xxl-3 col-xl-3 col-lg-3 col-sm-6 custom-pad-20" v-for="item in serviceBox" :key="item.title">
                <div class="kservice text-center mb-20">
                    <div class="kservice-icon">
                        <i><font-awesome-icon :icon="item.f_icon" /></i>
                    </div>
                    <div class="kservice-content">
                        <h5 class="kservice-content-title">
                            <NuxtLink :to="item.url" v-html="item.serviceBoxTitle">{{ item.serviceBoxTitle }}</NuxtLink>
                        </h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
<!-- service area end here -->
</template>

<script>
export default {
    name: 'Service',
    data() {
        return {
            sectionSubTitle: 'All Categories List',
            sectionTitle: 'The Services <br>We’re Offering',
            descripionText: 'There are many variations of passages of lorem ipsum available but the majority have suffered alteration in some form by injected humour.',
            serviceBox: [{
                    serviceBoxTitle: 'Website <br>Development',
                    url: '/servicedetails',
                    f_icon: ['far', 'edit'],
                },
                {
                    serviceBoxTitle: 'Graphic <br>Designing',
                    url: '/servicedetails',
                    f_icon: ['far', 'paper-plane'],
                },
                {
                    serviceBoxTitle: 'SEO & Content <br>writting',
                    url: '/servicedetails',
                    f_icon: ['far', 'chart-bar']
                },
                {
                    serviceBoxTitle: 'Digital <br>marketing',
                    url: '/servicedetails',
                    f_icon: ['far', 'handshake']
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
