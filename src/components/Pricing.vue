<script setup>
const pricing = {
    title: 'Upgrade to Pro',
    subtitle: 'PRICING',
    items: [
        {
            title: 'PERSONAL',
            price: 14,
            currencySymbol: '$',
            duration: 'm',
            features: [
                    { name: '10 Projects', status: 'available' },
                    { name: '5 GB Storage', status: 'available' },
                    { name: 'Basic Support', status: 'available' },
                    { name: 'Collaboration', status: 'notAvailable' },
                    { name: 'Reports and analytics', status: 'notAvailable' },
                ],
        }, {
            title: 'FOR TEAMS',
            price: 29,
            currencySymbol: '$',
            duration: 'm',
            features: [
                    { name: 'Unlimited Projects', status: 'available' },
                    { name: '100 GB Storage', status: 'available' },
                    { name: 'Priority Support', status: 'available' },
                    { name: 'Collaboration', status: 'available' },
                    { name: 'Reports and analytics', status: 'available' },
                ],
        }, {
            title: 'ENTERPRISE',
            price: 249,
            currencySymbol: '$',
            duration: 'm',
            features: [
                    { name: 'Unlimited Projects', status: 'available' },
                    { name: 'Unlimited Storage', status: 'available' },
                    { name: 'Priority Support', status: 'available' },
                    { name: 'Collaboration', status: 'available' },
                    { name: 'Reports and analytics', status: 'available' },
                    { name: 'Web hooks', status: 'available' },
                ],
        },

    ]
    
}
</script>

<template>
    
          <div class="section" id="pricing">
              <div class="container">
                  <div class="section-title">
                      <small>{{ pricing.subtitle }}</small>
                      <h3>{{ pricing.title }}</h3>
                  </div>

                  <div class="card-deck">
                      <div v-for="(item, index) in pricing.items" :key="index" class="card pricing">
                          <div class="card-head">
                              <small class="text-primary">{{ item.title }}</small>
                              <span class="price">{{ item.currencySymbol+item.price  }}/<sub>{{ item.duration }}</sub></span>
                          </div>
                          <ul class="list-group list-group-flush">
                              <div class="list-group-item" v-for="(feature, index) in item.features" :key="index" v-html="'available' == feature.status ? feature.name : '<del>'+ feature.name+ '</del>' "></div>
                          </ul>
                          <div class="card-body">
                              <a href="#" class="btn btn-primary btn-lg btn-block">Choose this Plan</a>
                          </div>
                      </div>
                      
                  </div>
                  <!-- // end .pricing -->


              </div>

          </div>
</template>

<style>

@media (max-width:992px) {
    .card-deck {
        -ms-flex-direction: column;
        flex-direction: column;
    }
    .card-deck .card {
        margin-bottom: 15px;
    }
}

.card.pricing {
    border: 1px solid #f1eef1;
}

.card.pricing.popular {
    border-top-width: 3px;
    border-color: #ce75b4 #faf6fb #FFF;
    box-shadow: 0px 12px 59px 0px rgba(36, 7, 31, 0.11);
    color: #633991;
}

.card.pricing .card-head {
    text-align: center;
    padding: 40px 0 20px;
}

.card.pricing .card-head .price {
    display: block;
    font-size: 45px;
    font-weight: 300;
    color: #633991;
}

.card.pricing .card-head .price sub {
    bottom: 0;
    font-size: 55%;
}

.card.pricing .list-group-item {
    border: 0;
    text-align: center;
    color: #959094;
    padding: 1.05rem 1.25rem;
}
.card.pricing .list-group-item del {
    color: #d9d3d8;
}
.card.pricing .card-body {
    padding: 1.75rem;
}
</style>