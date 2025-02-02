// script.js
let cart = [];

function updateCart() {
    const cartCount = document.getElementById("cart-count");
    cartCount.textContent = cart.length;
}

document.querySelectorAll(".add-to-cart").forEach(button => {
    button.addEventListener("click", function() {
        const productId = this.getAttribute("data-product");
        cart.push(productId);
        updateCart();
        alert("Product added to cart!");
    });
});

document.addEventListener("DOMContentLoaded", function() {
    updateCart();  // Initial cart count
});
