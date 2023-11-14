<script setup>

// const company_name = {
//     name: 'Doofaz It',
//     url: 'index.html'
// };

// const menus = [
//     { name: 'Home', url: 'index.html' },
//     { name: 'Resume', url: 'resume.html' },
//     { name: 'Projects', url: 'project.html' },
//     { name: 'Contact', url: 'contact.html' },
// ];

const header_data = {
    company_name:{name:'Doofaz IT', url:'index.html'},
    menus: [
    { name: 'Home', url: 'index.html' },
    { name: 'Resume', url: 'resume.html' },
    { name: 'Projects', url: 'project.html' },
    { name: 'Contact', url: 'contact.html' },
    ]

}

</script>

<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-white py-3">
        <div class="container px-5">
            <a class="navbar-brand" :href="header_data.company_name.url"><span class="fw-bolder text-primary">{{ header_data.company_name.name }}</span></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ms-auto mb-2 mb-lg-0 small fw-bolder">

                    <li v-for="menu in header_data.menus" :key="menu.name" class="nav-item">
                        <a class="nav-link" :href="menu.url">{{ menu.name }}</a>
                    </li>
                    
                </ul>
            </div>
        </div>
    </nav>
</template>