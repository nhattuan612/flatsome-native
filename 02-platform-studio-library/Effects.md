# Effects

Data-driven effect map scanned from `337` harvested unique exports in `data/flatsome-studio/exports (ngoài hub)`.

## Coverage

- Scope: visual treatment, motion, hover, slider behavior, and video-related attributes found in harvested Flatsome Studio exports.
- Status: `core effect coverage upgraded` from spot-check list to grouped operating map.
- Goal: help Codex and workers choose native Flatsome effects without falling back to HTML for presentation behavior.
- Note: this file maps `shortcode/native attributes` observed in exports, not every hidden JS effect inside the Flatsome runtime.

## Overlay and Contrast

### `dark`

- Observed uses: `325`
- Common values: `true` (325)
- Example: `1000` eCommerce 3-Column Banner: `[section label="Call to Action" bg_color="rgb(18, 18, 18)" dark="true" padding="0px"]`
- Example: `10735` Sign Up: Color Banner With Form: `[section label="Subscribe" bg="{{{20721}}}" bg_overlay="rgba(0, 100, 154, 0.7)" bg_pos="65% 73%" dark="true" padding="175px" padding__sm="80px" padding__md="135px"]`

### `bg_overlay`

- Observed uses: `200`
- Common values: `rgba(0, 0, 0, 0.3)` (21), `rgba(0, 0, 0, 0.1)` (18), `rgba(0, 0, 0, 0.15)` (12), `rgba(0, 0, 0, 0.4)` (12), `rgba(0, 0, 0, 0.25)` (11), `rgba(0, 0, 0, 0.2)` (10), `rgba(0, 0, 0, 0.35)` (8), `rgba(111, 166, 212, 0.25)` (7)
- Example: `1000` eCommerce 3-Column Banner: `[ux_banner height="500px" height__sm="275px" height__md="500px" bg="{{{863}}}" bg_color="rgb(255, 255, 255)" bg_overlay="rgba(0, 0, 0, 0.58)" bg_pos="56% 43%"]`
- Example: `1000` eCommerce 3-Column Banner: `[ux_banner height="500px" height__sm="275px" bg="{{{863}}}" bg_color="rgb(255, 255, 255)" bg_overlay="rgba(255, 255, 255, 0.17)" bg_pos="72% 58%"]`

### `bg_overlay__sm`

- Observed uses: `9`
- Common values: `rgba(0, 0, 0, 0.3)` (2), `rgba(0, 0, 0, 0.15)` (2), `rgb(45, 78, 103)` (1), `rgba(0, 0, 0, 0.4)` (1), `rgba(0, 0, 0, 0.12)` (1), `rgba(0, 0, 0, 0.2)` (1), `rgba(255, 255, 255, 0.7)` (1)
- Example: `1165` eCommerce Banner Text Right: `[section label="Call to Action" bg="{{{21360}}}" bg_overlay="rgba(0, 0, 0, 0.15)" bg_overlay__sm="rgba(0, 0, 0, 0.3)" bg_pos="48% 34%" dark="true" height="500px"]`
- Example: `13586` Single Product: Focus: `[section label="Hero" bg="{{{13769}}}" bg_color="rgb(247, 245, 244)" bg_overlay="rgba(0, 0, 0, 0.5)" bg_overlay__sm="rgb(45, 78, 103)" bg_overlay__md="rgba(0, 0, 0, 0.5)" bg_pos="66% 65%" dark="true" padding="60px" height="600px" scroll_for_more="true"]`

### `bg_overlay__md`

- Observed uses: `11`
- Common values: `rgba(0, 0, 0, 0.3)` (3), `rgba(0, 0, 0, 0.5)` (2), `rgba(0, 0, 0, 0.09)` (2), `rgba(0, 0, 0, 0.21)` (1), `rgba(0, 0, 0, 0.1)` (1), `rgba(0, 0, 0, 0.33)` (1), `rgba(255, 255, 255, 0.2)` (1)
- Example: `13509` Landingpage: One-Pager Elemental: `[section label="Contact" bg="{{{13554}}}" bg_overlay__md="rgba(0, 0, 0, 0.5)" bg_pos="14% 53%" padding="100px"]`
- Example: `13586` Single Product: Focus: `[section label="Hero" bg="{{{13769}}}" bg_color="rgb(247, 245, 244)" bg_overlay="rgba(0, 0, 0, 0.5)" bg_overlay__sm="rgb(45, 78, 103)" bg_overlay__md="rgba(0, 0, 0, 0.5)" bg_pos="66% 65%" dark="true" padding="60px" height="600px" scroll_for_more="true"]`

### `image_overlay`

- Observed uses: `100`
- Common values: `rgba(253, 111, 94, 0.6)` (10), `rgba(0, 0, 0, 0.15)` (9), `rgba(38, 53, 70, 0.5)` (8), `rgba(0, 0, 0, 0.17)` (7), `rgba(253, 111, 94, 0.76)` (7), `rgba(0, 0, 0, 0)` (6), `rgba(244, 244, 244, 0.7)` (6), `rgba(42, 42, 42, 0.2)` (4)
- Example: `10633` Projects row with hover effect: `[ux_image_box style="overlay" img="{{{21708}}}" image_height="100%" image_overlay="rgba(39, 54, 70, 0.81)" image_hover="overlay-add" link="#" text_pos="middle" text_hover="slide"]`
- Example: `10633` Projects row with hover effect: `[ux_image_box style="overlay" img="{{{21623}}}" image_height="100%" image_overlay="rgba(39, 54, 70, 0.81)" image_hover="overlay-add" link="#" text_pos="middle" text_hover="slide"]`

## Motion and Reveal

### `animate`

- Observed uses: `103`
- Common values: `fadeInUp` (39), `bounceInUp` (27), `fadeInLeft` (13), `fadeInRight` (11), `fadeInDown` (7), `bounceIn` (3), `bounceInDown` (2), `none` (1)
- Example: `13586` Single Product: Focus: `[col_inner_1 span="4" span__sm="4" animate="bounceIn"]`
- Example: `13790` Landing Page: Shop - Focus: `[col_inner span="7" span__sm="12" force_first="small" animate="fadeInUp" class="home-photo-box-large"]`

### `parallax`

- Observed uses: `34`
- Common values: `7` (29), `6` (2), `9` (2), `3` (1)
- Example: `13509` Landingpage: One-Pager Elemental: `[section label="Quote" bg="{{{21174}}}" bg_overlay="rgba(0, 0, 0, 0.25)" bg_pos="53% 44%" parallax="7" dark="true" height="400px" height__sm="300px"]`
- Example: `13586` Single Product: Focus: `[section label="Icons + Background" bg="{{{13722}}}" bg_overlay="rgba(0, 0, 0, 0.1)" bg_overlay__sm="rgba(0, 0, 0, 0.4)" bg_pos="31% 69%" parallax="7" dark="true" padding="80px"]`

### `scroll_for_more`

- Observed uses: `19`
- Common values: `true` (19)
- Example: `13480` Landing Page: Clean Studio: `[section label="Hero" bg="{{{13482}}}" bg_overlay="rgba(0, 0, 0, 0.43)" bg_pos="50% 37%" dark="true" height="500px" scroll_for_more="true"]`
- Example: `13586` Single Product: Focus: `[section label="Hero" bg="{{{13769}}}" bg_color="rgb(247, 245, 244)" bg_overlay="rgba(0, 0, 0, 0.5)" bg_overlay__sm="rgb(45, 78, 103)" bg_overlay__md="rgba(0, 0, 0, 0.5)" bg_pos="66% 65%" dark="true" padding="60px" height="600px" scroll_for_more="true"]`

## Hover and Interactive States

### `image_hover`

- Observed uses: `198`
- Common values: `zoom` (92), `overlay-add` (49), `glow` (33), `fade-out` (9), `overlay-remove-50` (6), `color` (5), `overlay-add-50` (3), `zoom-fade` (1)
- Example: `10633` Projects row with hover effect: `[ux_image_box style="overlay" img="{{{21708}}}" image_height="100%" image_overlay="rgba(39, 54, 70, 0.81)" image_hover="overlay-add" link="#" text_pos="middle" text_hover="slide"]`
- Example: `10633` Projects row with hover effect: `[ux_image_box style="overlay" img="{{{21623}}}" image_height="100%" image_overlay="rgba(39, 54, 70, 0.81)" image_hover="overlay-add" link="#" text_pos="middle" text_hover="slide"]`

### `hover`

- Observed uses: `76`
- Common values: `glow` (28), `zoom` (21), `fade-out` (11), `overlay-remove` (6), `fade` (4), `bounce` (3), `overlay-add` (2), `zoom-long` (1)
- Example: `16470` Landing Page: Get Started: `[col_inner span="6" span__sm="12" span__md="10" bg_color="rgba(254, 254, 254, 0.06)" bg_radius="10" hover="fade" depth_hover="4"]`
- Example: `16579` Landing Page: Legacy: `[section bg="{{{16587}}}" bg_size="original" bg_overlay="rgba(0, 0, 0, 0.44)" bg_pos="42% 12%" hover="zoom-long" dark="true" padding__sm="100px" height="600px"]`

### `hover_alt`

- Observed uses: `1`
- Common values: `zoom` (1)
- Example: `18579` Landing Page: Wedding: `[ux_banner height="500px" bg="{{{18588}}}" hover="glow" hover_alt="zoom" link="#"]`

### `text_hover`

- Observed uses: `45`
- Common values: `slide` (26), `bounce` (12), `fade-out` (6), `invert` (1)
- Example: `10633` Projects row with hover effect: `[ux_image_box style="overlay" img="{{{21708}}}" image_height="100%" image_overlay="rgba(39, 54, 70, 0.81)" image_hover="overlay-add" link="#" text_pos="middle" text_hover="slide"]`
- Example: `13773` Info Cards: Mosaic: `[ux_image_box style="label" img="{{{13778}}}" link="#" text_align="left" text_hover="slide" text_bg="rgb(0, 0, 0)" text_color="dark"]`

### `border_hover`

- Observed uses: `8`
- Common values: `zoom-in` (6), `bounce` (2)
- Example: `15559` About Page: Story Telling: `[section label="Edit Border Color" border="0px 0px 0px 40px" border_color="rgb(111, 166, 212)" border_hover="bounce"]`
- Example: `17840` Wiki: Archive Landing Page: `[col span="2" span__sm="6" span__md="4" animate="bounceInUp" border="2px 2px 2px 2px" border_hover="zoom-in"]`

## Depth and Elevation

### `depth`

- Observed uses: `28`
- Common values: `2` (18), `3` (5), `1` (4), `5` (1)
- Example: `13790` Landing Page: Shop - Focus: `[col_inner span="5" span__sm="6" margin="-60px 0px 0px -130px" bg_color="rgb(255,255,255)" animate="fadeInLeft" depth="2" class="home-photo-box-small"]`
- Example: `15112` Testimonial: Double Column Callout: `[col span__sm="12" margin="60px 0px 40px 0px" depth="3"]`

### `depth_hover`

- Observed uses: `32`
- Common values: `4` (11), `1` (10), `3` (5), `0` (3), `5` (2), `2` (1)
- Example: `13509` Landingpage: One-Pager Elemental: `[col span="4" span__sm="12" bg_color="rgb(255,255,255)" depth_hover="4"]`
- Example: `14454` Pricing Page: Basic Plans: `[ux_price_table title="Mini" price="$20" description="Per month" radius="10" depth_hover="0"]`

## Slider and Carousel Behavior

### `timer`

- Observed uses: `52`
- Common values: `3000` (32), `4000` (12), `3500` (2), `2500` (2), `4500` (2), `2000` (1), `5000` (1)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `13509` Landingpage: One-Pager Elemental: `[ux_slider type="fade" arrows="false" timer="3000" pause_hover="false"]`

### `pause_hover`

- Observed uses: `39`
- Common values: `false` (39)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `13509` Landingpage: One-Pager Elemental: `[ux_slider type="fade" arrows="false" timer="3000" pause_hover="false"]`

### `auto_slide`

- Observed uses: `15`
- Common values: `3000` (11), `false` (3), `4000` (1)
- Example: `14650` Landingpage: Creative Agency: `[ux_instagram_feed username="buildinamsterdam" caption="0" type="slider" auto_slide="3000"]`
- Example: `15393` Blog Starter: `[blog_posts style="overlay" type="slider-full" slider_nav_style="simple" slider_bullets="true" auto_slide="3000" cat="77" posts="3" title_size="large" readmore="Read article" show_date="false" excerpt="false" show_category="text" image_height="400px" image_overlay="rgba(114, 114, 114, 0.3)" text_pos="middle" text_size="large"]`

### `hide_nav`

- Observed uses: `34`
- Common values: `true` (34)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `13586` Single Product: Focus: `[ux_slider style="focus" slide_width="80%" hide_nav="true" nav_style="simple" nav_color="dark" bullets="false" timer="3500" pause_hover="false"]`

### `nav_style`

- Observed uses: `44`
- Common values: `simple` (44)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `13586` Single Product: Focus: `[ux_slider style="focus" slide_width="80%" hide_nav="true" nav_style="simple" nav_color="dark" bullets="false" timer="3500" pause_hover="false"]`

### `nav_color`

- Observed uses: `21`
- Common values: `dark` (21)
- Example: `13586` Single Product: Focus: `[ux_slider style="focus" slide_width="80%" hide_nav="true" nav_style="simple" nav_color="dark" bullets="false" timer="3500" pause_hover="false"]`
- Example: `13782` Testimonial: Full Width Slider: `[ux_slider style="focus" nav_pos="outside" arrows="false" nav_style="simple" nav_color="dark" timer="4000"]`

### `nav_pos`

- Observed uses: `14`
- Common values: `outside` (14)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `13782` Testimonial: Full Width Slider: `[ux_slider style="focus" nav_pos="outside" arrows="false" nav_style="simple" nav_color="dark" timer="4000"]`

### `nav_size`

- Observed uses: `8`
- Common values: `normal` (7), `large` (1)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `14973` Testimonial: Section BG Slider: `[ux_slider nav_size="normal" nav_style="simple" bullet_style="square" timer="3000"]`

### `slider_nav_style`

- Observed uses: `13`
- Common values: `simple` (13)
- Example: `15393` Blog Starter: `[blog_posts style="overlay" type="slider-full" slider_nav_style="simple" slider_bullets="true" auto_slide="3000" cat="77" posts="3" title_size="large" readmore="Read article" show_date="false" excerpt="false" show_category="text" image_height="400px" image_overlay="rgba(114, 114, 114, 0.3)" text_pos="middle" text_size="large"]`
- Example: `15579` Product Duo Banner: `[ux_products col_spacing="collapse" columns="1" slider_nav_style="simple" slider_nav_color="light" slider_nav_position="outside" slider_bullets="true" auto_slide="3000" cat="55" products="4"]`

### `slider_nav_position`

- Observed uses: `7`
- Common values: `outside` (7)
- Example: `15579` Product Duo Banner: `[ux_products col_spacing="collapse" columns="1" slider_nav_style="simple" slider_nav_color="light" slider_nav_position="outside" slider_bullets="true" auto_slide="3000" cat="55" products="4"]`
- Example: `15590` Product Slider Title: `[ux_products columns__sm="2" columns__md="4" slider_nav_style="simple" slider_nav_position="outside" auto_slide="3000"]`

### `slider_nav_color`

- Observed uses: `2`
- Common values: `light` (2)
- Example: `15579` Product Duo Banner: `[ux_products col_spacing="collapse" columns="1" slider_nav_style="simple" slider_nav_color="light" slider_nav_position="outside" slider_bullets="true" auto_slide="3000" cat="55" products="4"]`
- Example: `17840` Wiki: Archive Landing Page: `[blog_posts style="shade" col_spacing="collapse" columns="1" columns__sm="1" columns__md="1" slider_nav_style="simple" slider_nav_color="light" auto_slide="3000" posts="3" show_date="false" show_category="text" image_height="100%" image_overlay="rgba(0, 0, 0, 0.22)"]`

### `slider_bullets`

- Observed uses: `10`
- Common values: `true` (10)
- Example: `15393` Blog Starter: `[blog_posts style="overlay" type="slider-full" slider_nav_style="simple" slider_bullets="true" auto_slide="3000" cat="77" posts="3" title_size="large" readmore="Read article" show_date="false" excerpt="false" show_category="text" image_height="400px" image_overlay="rgba(114, 114, 114, 0.3)" text_pos="middle" text_size="large"]`
- Example: `15579` Product Duo Banner: `[ux_products col_spacing="collapse" columns="1" slider_nav_style="simple" slider_nav_color="light" slider_nav_position="outside" slider_bullets="true" auto_slide="3000" cat="55" products="4"]`

### `bullets`

- Observed uses: `31`
- Common values: `false` (31)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `13586` Single Product: Focus: `[ux_slider style="focus" slide_width="80%" hide_nav="true" nav_style="simple" nav_color="dark" bullets="false" timer="3500" pause_hover="false"]`

### `bullet`

- Observed uses: `10`
- Common values: `false` (10)
- Example: `13586` Single Product: Focus: `[scroll_to title="buy-now" bullet="false"]`
- Example: `14063` Landing Page: Ebook: `[scroll_to title="sample" bullet="false"]`

### `bullet_style`

- Observed uses: `29`
- Common values: `simple` (24), `dashes-spaced` (2), `square` (2), `dashes` (1)
- Example: `13790` Landing Page: Shop - Focus: `[ux_slider label="Hero" hide_nav="true" arrows="false" nav_style="simple" bullet_style="dashes" timer="3500" pause_hover="false"]`
- Example: `13895` Slider: Section Boxed Focus: `[ux_slider style="focus" slide_width="75%" hide_nav="true" nav_style="simple" nav_color="dark" bullet_style="dashes-spaced"]`

### `freescroll`

- Observed uses: `2`
- Common values: `true` (2)
- Example: `10722` Clients row slider: `[ux_slider style="focus" freescroll="true" hide_nav="true" nav_pos="outside" nav_size="normal" nav_style="simple" bullets="false" timer="4000" pause_hover="false"]`
- Example: `16322` Landing Page: Shop - Simple Funk: `[ux_slider style="container" freescroll="true" hide_nav="true" nav_size="normal" nav_style="simple" bullet_style="simple" timer="3000" pause_hover="false"]`

## Video Behavior

### `video`

- Observed uses: `1`
- Common values: `#` (1)
- Example: `18429` Landing Page: Shop - Coffee: `[video_button video="#"]`

### `video_mp4`

- Observed uses: `4`
- Common values: `https://cdn.shopify.com/s/files/1/0016/0959/6989/files/ROOM_homepage_product_Desktop_and_mobile.mp4` (1), `https://cdn.webshopapp.com/shops/283663/files/296538447/access.mp4` (1), `https://srv-file9.gofile.io/download/9XkZ7z/video.mp4` (1), `https://demos.uxthemes.com/layouts/wp-content/uploads/sites/17/2020/06/Pexels-Videos-3414.mp4` (1)
- Example: `13586` Single Product: Focus: `[ux_banner height="300px" bg="{{{13747}}}" bg_color="rgb(247, 245, 244)" video_mp4="https://cdn.shopify.com/s/files/1/0016/0959/6989/files/ROOM_homepage_product_Desktop_and_mobile.mp4"]`
- Example: `14537` Landing Page: Shop - Sidebar Drop: `[section bg="{{{14853}}}" bg_color="rgb(242, 242, 242)" bg_overlay="rgba(0, 0, 0, 0.35)" dark="true" padding="80px" video_mp4="https://cdn.webshopapp.com/shops/283663/files/296538447/access.mp4"]`

### `video_visibility`

- Observed uses: `3`
- Common values: `visible` (3)
- Example: `13586` Single Product: Focus: `[ux_banner label="Photo *Mobile Only" bg="{{{13589}}}" bg_color="rgb(247, 245, 244)" video_visibility="visible" visibility="show-for-small"]`
- Example: `16007` Coming Soon: Hello Subscriber: `[section bg="{{{16024}}}" padding="0px" video_visibility="visible"]`

## Official Demo Confirmations Beyond Harvested Exports

These confirmations come from official Flatsome demo surfaces rather than from the harvested `337` export set above.

Use this section for operating awareness, not for pretending the harvested attribute counts cover everything.

### `sticky section`

- Status:
  - official demo confirmed
- Meaning:
  - sticky behavior is part of the intended native section toolset and should be considered before custom JS/CSS workarounds

### `section masks`

- Status:
  - official demo and feature pages confirm the surface exists
- Meaning:
  - section transitions can be treated as native visual language, not only custom SVG/CSS decoration

### `lightbox behavior`

- Status:
  - official demo confirmed
- Meaning:
  - media enlargement and modal reveal are part of native interaction options

### `hotspot interaction`

- Status:
  - official demo confirmed
- Meaning:
  - interactive anchors on image surfaces are part of the official visual storytelling surface

### `flip book interaction`

- Status:
  - official demo confirmed
- Meaning:
  - card/image flip interaction is a native presentation option worth considering before HTML-heavy hover effects

### `video button surface`

- Status:
  - official demo confirmed
- Meaning:
  - native video trigger surfaces exist even when full custom embed shells are unnecessary
