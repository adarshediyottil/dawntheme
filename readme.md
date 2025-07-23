# Shopify Dawn Theme – Related Products as Bundles

This custom Dawn theme setup allows you to assign related products to any individual product using Shopify **metafields**. These related products will appear on the frontend as a bundled section below the main product, enhancing cross-sell opportunities.

---

## 🛒 Live Store Details

- **Frontend URL**: [https://ediyottil.myshopify.com/](https://ediyottil.myshopify.com/) password: 1234
- **Sample Product**: [Bangle Bracelet](https://ediyottil.myshopify.com/products/bangle-bracelet)

---

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

   - Look for a metafield named something like `Related Products (Bundle)` or `related_products_custom`.
   - Choose one or more products to relate as bundles.

5. **Save Changes**  
   Click **Save** to apply the metafield assignments.

---

## ✅ View on Frontend

1. Go to the frontend product page (e.g., [Bangle Bracelet](https://ediyottil.myshopify.com/products/bangle-bracelet)).
2. Scroll down below the main product details.
3. You’ll see a **Related Products Bundle** section displaying the metafield-assigned products.

---

## 📂 Files Modified in the Dawn Theme

> Below are the theme files that were updated to enable the related bundle feature.

- `sections/main-product.liquid`  
  *(Add the following code below "blocks": [)*

   {
      "type": "related_products",
      "name": "Custom Related Products",
      "settings": [
        {
          "type": "text",
          "id": "heading",
          "label": "Heading",
          "default": "Related Products"
        },
    	{
          "type": "number",
          "id": "heading_font_size",
          "label": "Heading font size (px)",
          "default": 18
        },
        {
          "type": "color",
          "id": "heading_color",
          "label": "Heading color",
          "default": "#121212"
        }
      ]
    },

-  `sections/main-product.liquid`   
  *Liquid code for main-product.liquid file
Add the following code below {%- case block.type -%}*

line from 91 to 317

---

## 🧪 Sample Metafield Definition

To define the metafield in your Shopify admin:

1. Go to `Settings` → `Custom Data` → `Products`
2. Add a new metafield definition:
   - **Name**: `Related Products Custom`
   - **Namespace and key**: `custom.related_products`
   - **Content Type**: `Product List`
   - Save

---

## 💡 Notes

- Make sure the assigned products are **active** and **available on the online store** channel.
- For better user experience, consider adding checkboxes or quantity selectors in the bundle section.

---

## 📬 Contact

For any issues or enhancements, contact the developer at: **adarsh.ediyottil@gmail.com**
