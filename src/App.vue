<template>
    <app-navigation />

    <div class="container-fluid">
        <div class="row">
            <menu-bar />

            <main role="main" class="col-md-9 ml-sm-auto col-lg-10 px-md-4">
                <div
                    style="
                        position: absolute;
                        inset: 0px;
                        overflow: hidden;
                        pointer-events: none;
                        visibility: hidden;
                        z-index: -1;
                    "
                    class="chartjs-size-monitor"
                >
                    <div
                        class="chartjs-size-monitor-expand"
                        style="
                            position: absolute;
                            left: 0;
                            top: 0;
                            right: 0;
                            bottom: 0;
                            overflow: hidden;
                            pointer-events: none;
                            visibility: hidden;
                            z-index: -1;
                        "
                    >
                        <div
                            style="
                                position: absolute;
                                width: 1000000px;
                                height: 1000000px;
                                left: 0;
                                top: 0;
                            "
                        ></div>
                    </div>
                    <div
                        class="chartjs-size-monitor-shrink"
                        style="
                            position: absolute;
                            left: 0;
                            top: 0;
                            right: 0;
                            bottom: 0;
                            overflow: hidden;
                            pointer-events: none;
                            visibility: hidden;
                            z-index: -1;
                        "
                    >
                        <div
                            style="
                                position: absolute;
                                width: 200%;
                                height: 200%;
                                left: 0;
                                top: 0;
                            "
                        ></div>
                    </div>
                </div>
                <h2>Section title</h2>
                <div class="table-responsive">
                    <table class="table table-striped table-sm">
                        <thead>
                            <tr>
                                <th>#</th>
                                <th>Header</th>
                                <th>Header</th>
                                <th>Header</th>
                                <th>Header</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>1,001</td>
                                <td>Lorem</td>
                                <td>ipsum</td>
                                <td>dolor</td>
                                <td>sit</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </main>
        </div>
    </div>
</template>

<script>
import AppNavigation from '@/components/AppNavigation.vue';
import MenuBar from '@/components/MenuBar.vue';

export default {
    components: {
        AppNavigation,
        MenuBar,
    },
};
</script>

<style>
body {
    font-size: 0.875rem;
}

.feather {
    width: 16px;
    height: 16px;
    vertical-align: text-bottom;
}

/*
 * Sidebar
 */

.sidebar {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    z-index: 100; /* Behind the navbar */
    padding: 48px 0 0; /* Height of navbar */
    box-shadow: inset -1px 0 0 rgba(0, 0, 0, 0.1);
}

@media (max-width: 767.98px) {
    .sidebar {
        top: 5rem;
    }
}

.sidebar-sticky {
    position: relative;
    top: 0;
    height: calc(100vh - 48px);
    padding-top: 0.5rem;
    overflow-x: hidden;
    overflow-y: auto; /* Scrollable contents if viewport is shorter than content. */
}

@supports ((position: -webkit-sticky) or (position: sticky)) {
    .sidebar-sticky {
        position: -webkit-sticky;
        position: sticky;
    }
}

.sidebar .nav-link {
    font-weight: 500;
    color: #333;
}

.sidebar .nav-link .feather {
    margin-right: 4px;
    color: #999;
}

.sidebar .nav-link.active {
    color: #007bff;
}

.sidebar .nav-link:hover .feather,
.sidebar .nav-link.active .feather {
    color: inherit;
}

.sidebar-heading {
    font-size: 0.75rem;
    text-transform: uppercase;
}

/*
 * Navbar
 */

.navbar-brand {
    padding-top: 0.75rem;
    padding-bottom: 0.75rem;
    font-size: 1rem;
    background-color: rgba(0, 0, 0, 0.25);
    box-shadow: inset -1px 0 0 rgba(0, 0, 0, 0.25);
}

.navbar .navbar-toggler {
    top: 0.25rem;
    right: 1rem;
}

.navbar .form-control {
    padding: 0.75rem 1rem;
    border-width: 0;
    border-radius: 0;
}

.form-control-dark {
    color: #fff;
    background-color: rgba(255, 255, 255, 0.1);
    border-color: rgba(255, 255, 255, 0.1);
}

.form-control-dark:focus {
    border-color: transparent;
    box-shadow: 0 0 0 3px rgba(255, 255, 255, 0.25);
}
</style>
