## Errors fixed in the Code and its description and solution

### CC-01 — "not appearing first dish name"

**Reproduced:** I start typing a dish name and the list of suggestions comes up, but 
                it's stuck behind the rest of the page. I can only click the very top 
                bit of it. The rest I can see, sort of, but clicking does nothing."

**Cause:** the majar cause the value of z index as z index controls which element appears in front of other.

**Fix:** we changed the value of z index from 1 to 45.

**Checked:** after running the overlapping is solved.

**Time:** it took about 15 min to solve.

## CC-02 — "not a readable text"

**Reproduced:**"I switched the site to dark mode and now the dish names and the prices are 
                almost invisible. The grey line under the name is fine, 
                it's just the name and the price."

**Cause:** previously the color of the text was color: #2b2118; which made text not readable;

**Fix:** we changed the color to ink color which made the color match with upper given color

**Checked:** code was run and text was visible;

**Time:**10 min was taken to solve.

# CC-06 — "accepting the value than is not in stock"

**Reproduced:**""The counter says only 2 samosas were left but it let me order 5, and 
                the order went through fine. When I got there they only had 2?"

**Cause:** .Due to absence of condition that quantity is less than or equal to stock

**Fix:** . we added the condition to check that quantity is less than stock value.

**Checked:**.we tried to add the quantity more than stock which was not accepted now.

**Time:** 40 min was taken to solve.

# CC-07 -"Cancelling makes it worse"

**Reproduced:** When the student cancels the order the quantity deducted during the order is 
                not returned to the stock amount available.

**Fix:**  Changed the stock calculation in releaseStock() from subtraction to addition 

**Checked:** we tried to order the meal and cancelled it the quantity was again added to amount of original stock 

**Time:** 20 mins was taken to solve

# CC-08: "An old coupon still works".

**Reproduced:** The coupon FRESHERS24 had expired, but still system accepts that old coupon 
                and applies discount.

**Cause:** Because Coupon() in pricing.js did not check the coupon's expiry date.

**Fix:** Added an expiry date check inside applyCoupon() before calculating discount 

**Checked:** now the old coupon is not getting applied.

**Time:** 20 min was taken


# CC-09 "showing long list instead of loading few"

**Reproduced:** The page displays a long list of dishes immediately instead of loading a few initially and loading more as the user scrolls.

**Cause:** Incorrect use of variables caused all the dishes to be displayed.

**Fix:** Changed  list to items in search.js so that only the dishes selected for the current page are returned.

**Checked:** now it is loading other dishes when scrolled down and showing 5 dishes before scrolling.

**Time:** 15 min was taken


### CC-10: "Sorting by price is backwards"


**Reproduced:** After picking low to high it shows most expensive thing on top of the list 

**Cause:** the comparison logic for price of low to high was reversed 

**Fix:** Changed the price-asc to a.price-b.price and price -desc to b.price-a.price.

**Checked:** now it shows correct order of display acc to cost 

**Time:** 30 min was taken to solve