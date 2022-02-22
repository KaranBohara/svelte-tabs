<script>
let logo= "assets/flame-logo.png";
</script>

<div class="navbar-container">
<div class="logo-bar"><img src={logo} alt="" width="50px" height="50px"/></div>
<div class="menu-bar">
    <li>Home</li>
    <li>About Us</li>
    <li>Contact</li>
    <li>Tabs</li>
    <li>My Profile</li>
</div>
</div>
<style>
.navbar-container
{
    height: 5rem;
    width:100%;
    background-color: #563D7C;
    display: flex;
}
.logo-bar
{
 width: 20%;
 display: flex;
 justify-content: center;
 align-items: center;
 height: 100%;
}
.menu-bar
{
width: 75%;
display: flex;
 justify-content: flex-end;
 align-items: center;
 height: 100%;
 color: white;
}
.menu-bar li{
    list-style: none;
    padding: 0rem 1.5rem;
    cursor: pointer;
}
</style>