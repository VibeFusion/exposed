# exposed
class UninstalledJob < ActiveJob::Base def perform(shop_domain:, webhook:) shop = Shop.find_by(shopify_domain: shop_domain) unless shop.nil? shop.destroy end end
