<template>
   <aside class="menu-sidebar d-none d-lg-block">
            <div class="logo">
                <a href="#">
                    <img src="interface/images/icon/logo.png" alt="Cool Admin" />
                </a>
            </div>
            <div class="menu-sidebar__content js-scrollbar1">
                <nav class="navbar-sidebar">
                    <ul class="list-unstyled navbar__list">
            
                        <li>
                            <a href="chart.html">
                                <i class="fas fa-chart-bar"></i>Charts</a>
                        </li>
                        <li class="active">
                            <a href="table.html">
                                <i class="fas fa-table"></i>Tables</a>
                        </li>
                        <li>
                            <a href="form.html">
                                <i class="far fa-check-square"></i>Forms</a>
                        </li>
                        <li>
                            <a href="calendar.html">
                                <i class="fas fa-calendar-alt"></i>Calendar</a>
                        </li>
                        <li>
                            <a href="map.html">
                                <i class="fas fa-map-marker-alt"></i>Maps</a>
                        </li>
                       
                    </ul>
                </nav>
            </div>
        </aside>
</template>

<script>
export default {
name:"Sidebar"
}
</script>

<style scoped>
.navbar-sidebar {
    padding: 0px!important;
    padding-bottom: 0;
}

ul.list-unstyled.navbar__list li {
    list-style: none;
    border: 1px solid #9a9a8626;
    width: 100%;
}

.navbar-sidebar .navbar__list li a {
    display: block;
    color: #555;
    font-size: 16px;
    padding: 15px 0;
    text-decoration: none;
}
</style>