# Salecto_Luma
Create Child theme from Luma and modify home page and product page.

### Installation

 - Unzip the zip file in `app/design/frontend/Salecto/luma_child`
 - Run Below commands:
 
  `php bin/magento c:c`
  `php bin/magento c:f`

- Assign the theme from `design >> configuration`
 
 If some content not display on home page then create new widget for child theme.

Create textarea product attribute with code "custom_message".

It will display on both list and details page.

To display slick products content

check file at `app/design/frontend/Salecto/luma_child/Magento_Theme/templates/html/slick.phtml`

Create Block from admin with identifier `block_footer_slick_content`

Add below content in it:

`<p>{{widget type="Magento\CatalogWidget\Block\Product\ProductsList" title="Slick Products" show_pager="0" products_count="12" template="Magento_CatalogWidget::product/widget/content/slider_grid.phtml" conditions_encoded="^[`1`:^[`type`:`Magento||CatalogWidget||Model||Rule||Condition||Combine`,`aggregator`:`all`,`value`:`1`,`new_child`:``^],`1--1`:^[`type`:`Magento||CatalogWidget||Model||Rule||Condition||Product`,`attribute`:`category_ids`,`operator`:`==`,`value`:`23`^]^]"}}</p>`

Your slick products carousal will be come from:

`app/design/frontend/Salecto/luma_child/Magento_CatalogWidget/templates/product/widget/content/slider_grid.phtml`
  
<p><img src="https://i.ibb.co/QKPy6JJ/Home-Page.png"></p>
<p><img src="https://i.ibb.co/bLQqJWF/Home-Page.png"></p>
<p><img src="https://i.ibb.co/TKWT8dj/Screenshot-from-2021-02-25-20-08-56.png"></p>
<p><img src="https://i.ibb.co/5nLNX5F/Screenshot-from-2021-02-25-20-09-01.png"></p>
<p><img src="https://i.ibb.co/HG5pqGh/Screenshot-from-2021-02-25-20-09-18.png"></p>
<p><img src="https://i.ibb.co/P90wvgL/Bras-Tanks-Tops-Women.png"></p>
<p><img src="https://i.ibb.co/S7D9NvD/Breathe-Easy-Tank.png"></p>
