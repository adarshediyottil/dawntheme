# Shopify Dawn Theme – Related Products as Bundles

This custom Dawn theme setup allows you to assign related products to any individual product using Shopify **metafields**. These related products will appear on the frontend as a bundled section below the main product, enhancing cross-sell opportunities.

---

## 🛒 Live Store Details

* **Frontend URL**: [https://ediyottil.myshopify.com/](https://ediyottil.myshopify.com/)
  Password: `1234`
* **Sample Product**: [Bangle Bracelet](https://ediyottil.myshopify.com/products/bangle-bracelet)

---

## 🔧 How to Add Related Products as Bundles

1. **Login to Shopify Admin**
   Go to: [https://ediyottil.myshopify.com/admin](https://ediyottil.myshopify.com/admin)

2. **Navigate to Products**
   From the sidebar, go to `Products`.

3. **Select a Product**
   Click on the product for which you want to assign bundle items.

4. **Assign Products to Metafield**
   Scroll down to the **Metafields** section (usually at the bottom of the product page).

   * Look for a metafield named `Related Products Custom`.
   * Choose one or more products to relate as bundles.

5. **Save Changes**
   Click **Save** to apply the metafield assignments.

---

## 🧱 Metafield Configuration

To implement the metafield used for assigning related products, follow these steps:

1. Go to **Settings** → **Custom Data** → **Products**
2. Click **Add definition**
3. Configure the metafield as follows:

   * **Name**: `Related Products Custom`
   * **Namespace and key**: `custom.related_products`
   * **Content type**: **Product List**
   * Click **Save**

This metafield enables the selection of multiple products to be associated with another product as bundles.

---

## ✅ View on Frontend

1. Visit a product page (e.g., [Bangle Bracelet](https://ediyottil.myshopify.com/products/bangle-bracelet))
2. Scroll below the product details
3. The **Related Products Bundle** section will display the metafield-assigned products

---

## 📂 Files Modified in the Dawn Theme

> Below are the theme files that were updated to enable the related bundle feature.

* `sections/main-product.liquid`

  * Added schema block for related products (inside `"blocks": [ ... ]`)
  * Injected custom Liquid logic (from line 91 to 317) to display related product bundles using metafield values

---

## 💡 Notes

* Ensure the assigned products are **active** and **available on the Online Store** channel.
* For better UX, you can include quantity selectors and checkboxes in the bundle section.
* Works seamlessly with the latest version of Dawn Theme.

---

## 📬 Contact

For any issues, suggestions, or enhancements, feel free to reach out:

📧 **[adarsh.ediyottil@gmail.com](mailto:adarsh.ediyottil@gmail.com)**

