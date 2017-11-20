# frozen_string_literal: true
source 'https://rubygems.org'
ruby '2.3.1'

group :development, :test, :production, :preprod do
  gem 'rails','5.0.0.1'
  gem 'active_model_serializers','0.10.2'
  gem 'mysql2','~> 0.4'
  gem 'delayed_job_active_record','4.1.1'

  # paginatie gems, pk uitgezet, vooralsnog geen paginatie
  gem 'will_paginate', '3.1.0'
  gem 'api-pagination','4.4.0'

  # voor verbeterde API responses
  gem 'responders','2.3.0'

  # dit is een API, die moet dus juist geen cross origin policy hebben
  # pk, is dat zo? Volgens mij moeten we in productie juist vanaf hetzelfde domein komen?
  gem 'rack-cors','0.4.0'

  # met deze gem kunnen we XML decoderen
  gem 'libxml-ruby'

  # password hashing, nog steeds de beste keuze
  gem 'bcrypt-ruby'

  #gem voor json webtokens, zie https://jwt.io/ en https://github.com/jwt/ruby-jwt
  gem 'jwt'

  # Excelsheets voor compatiblity met XF
  gem 'roo'

  #voor het wegscrhijven van Excel bestanden (exports dus), kan niet met Roo  voor compatiblity met XF
  gem 'spreadsheet','1.0.1'
  #idem, alleen nu een snelle implementatie en voor xlsx ondersteuning
  gem 'xlsxtream'

  # gem voor barcode generatie
  gem 'barby'

  # QR code generator
  gem 'rqrcode'

  #verplichte js interpreter, alternatief voor nodejs
  gem 'therubyracer'

  #woordafbreking
  gem 'text-hyphen'

end

group :development, :test do
  # testing/specs
  # we gebruiken minitest, deze is ingebouwd in rails zelf
end

group :development do
  # devserver
  gem 'puma','~> 3.6.0'

  # listens to changes in your files and reloads
  gem 'listen', '~> 3.1.5'

  # Spring speeds up development by keeping your application running in the background. Read more: https://github.com/rails/spring
  gem 'spring','~> 1.7'
  gem 'spring-watcher-listen', '~> 2.0.0'

  # uitgeschakeld in afwachting van integratie met HG (nu alleen Git)
  # codeclimate tools waarmee we on-the-fly de gemaakte wijzigingen kunnen checken
  gem 'pronto'

  # de "runners" voor pronto
  gem 'pronto-rubocop', require: false
  gem 'pronto-brakeman', require: false
  gem 'pronto-reek', require: false
  gem 'pronto-flay', require: false
  gem 'pronto-fasterer', require: false
  gem 'pronto-rails_best_practices', require: false

  # code scaffolden adhv de bestaande DB
  # eenmalig inzetten, eigenlijk niet zo mooi
  # gem 'schema_to_scaffold'

  # documentatie
  gem 'yard','0.9.5'

  # wellicht handig op termijn
  # gem 'web-console'
end

group :production do
  # monitoring, inschakelen als we in productie gaan
  # gem 'rollbar'

  #applicatie monitoring voor Scout
  # gem 'scout_apm'
end
