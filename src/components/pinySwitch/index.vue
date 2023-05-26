<template>
    <div class="pithy-switch">
        <a-layout>
            <!-- Header section -->
            <a-layout-header class="pithy-switch-header">
                <a-row :gutter="16" align="middle">
                    <!-- Logo section within header -->
                    <a-col :span="4">
                        <div class="pithy-switch-header-logo">
                            <a-avatar :size="64" icon="user" />
                        </div>
                    </a-col>
                    <!-- Menu section within header -->
                    <a-col :span="20">
                        <div class="pithy-switch-header-menu">
                            <a-menu mode="horizontal" :default-selected-keys="['1']">
                                <a-menu-item key="1">Home</a-menu-item>
                                <a-menu-item key="2">About</a-menu-item>
                                <a-menu-item key="3">Contact</a-menu-item>
                            </a-menu>
                        </div>
                    </a-col>
                </a-row>
            </a-layout-header>
            <!-- Content section -->
            <a-layout-content class="pithy-switch-content">
                <a-row :gutter="16" align="middle">
                    <!-- Title section within content -->
                    <a-col :span="24">
                        <div class="pithy-switch-content-title">
                            <h1>Pithy Switch</h1>
                        </div>
                    </a-col>
                    <!-- Switch section within content -->
                    <a-col :span="24">
                        <div class="pithy-switch-content-switch">
                            <a-switch :default-checked="true" />
                        </div>
                    </a-col>
                    <!-- Description section within content -->
                    <a-col :span="24">
                        <div class="pithy-switch-content-description">
                            <p>Simple and easy-to-use switch component for your web applications.</p>
                        </div>
                    </a-col>
                </a-row>
            </a-layout-content>
            <!-- Footer section -->
            <a-layout-footer class="pithy-switch-footer">
                <a-row :gutter="16" align="middle">
                    <!-- Links section within footer -->
                    <a-col :span="24">
                        <div class="pithy-switch-footer-links">
                            <a href="#">Terms of Service</a> | <a href="#">Privacy Policy</a>
                        </div>
                    </a-col>
                </a-row>
            </a-layout-footer>
        </a-layout>
    </div>
</template>

<script>
import { Layout, LayoutHeader, LayoutContent, LayoutFooter, Row, Col, Menu, MenuItem, Switch, Avatar } from 'ant-design-vue';

export default {
    name: 'PithySwitch',
    components: {
        ALayout: Layout,
        ALayoutHeader: LayoutHeader,
        ALayoutContent: LayoutContent,
        ALayoutFooter: LayoutFooter,
        ARow: Row,
        ACol: Col,
        AMenu: Menu,
        AMenuItem: MenuItem,
        ASwitch: Switch,
        AAvatar: Avatar,
    },
};
</script>

<style>
.pithy-switch {
    display: flex;
    flex-direction: column;
    height: 100%;
}

.pithy-switch-header {
    background-color: #fff;
    padding: 0;
}

.pithy-switch-header-logo {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 64px;
}

.pithy-switch-header-menu {
    display: flex;
    justify-content: flex-end;
}

.pithy-switch-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-grow: 1;
}

.pithy-switch-content-title {
    margin-bottom: 16px;
}

.pithy-switch-content-switch {
    margin-bottom: 16px;
}

.pithy-switch-footer {
    background-color: #fff;
    padding: 0;
}

.pithy-switch-footer-links {
    text-align: center;
}
</style>
