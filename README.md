# compliance_poc
Check for Compliance Policy Results as per Stripe's Marketing Treasury doc \n

Steps for Running \n
1. Git Clone \n
2. sudo docker-compose up -d --build api_gateway \n

Live API ENDPoint 
curl -X POST "http://20.80.46.130:8081/internal/compliance_testing/analyse/website" \
  -H "Accept: */*" \
  -H "Content-Type: application/json" \
  -d '{"url":"https://www.joinguava.com/"}'

Expected Response \n

{
  "response": "Non-compliant findings:\n\n1. The use of the term \"banking\" in the phrase \"Guava is the digital banking and networking platform designed by and for Black small business owners.\" This could draw scrutiny from regulators as Guava is not a state- or federally-chartered bank or credit union.\n\n2. The use of the term \"banking platform\" in the phrase \"We're not just a banking platform.\" This could draw scrutiny from regulators as Guava is not a state- or federally-chartered bank or credit union.\n\n3. The use of the term \"business checking account\" in the phrases \"Create your business checking account for free in minutes with instant access to a virtual debit card.\" and \"Easily connect your business checking account to Venmo, Etsy, Shopify, Stripe, and more.\" This could draw scrutiny from regulators as Guava is not a state- or federally-chartered bank or credit union.\n\n4. The use of the term \"banking services\" in the phrase \"Guava is a financial technology company and is not a bank. Banking services provided by Piermont Bank, Member FDIC.\" This could draw scrutiny from regulators as Guava is not a state- or federally-chartered bank or credit union.\n\nSolutions:\n\n1. Replace the term \"banking\" with recommended terms like \"financial services\" or \"[Your brand] account\". For example, \"Guava is the digital financial services and networking platform designed by and for Black small business owners.\"\n\n2. Replace the term \"banking platform\" with recommended terms like \"financial platform\". For example, \"We're not just a financial platform.\"\n\n3. Replace the term \"business checking account\" with recommended terms like \"[Your brand] account\" or \"money management account\". For example, \"Create your Guava account for free in minutes with instant access to a virtual debit card.\" and \"Easily connect your Guava account to Venmo, Etsy, Shopify, Stripe, and more.\"\n\n4. Replace the term \"banking services\" with recommended terms like \"financial services\". For example, \"Guava is a financial technology company and is not a bank. Financial services provided by Piermont Bank, Member FDIC.\"",
  "status": 1
}