[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = JASONCHENG22.AU
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 udp_preference_limit = 1
 default_tgs_enctypes = arcfour-hmac
 default_tkt_enctypes = arcfour-hmac 

[realms] 
  JASONCHENG22.AU = {
  kdc = ip-172-31-30-195.us-west-2.compute.internal
  admin_server = ip-172-31-30-195.us-west-2.compute.internal
 }

[domain_realm]
   .us-west-2.compute.internal = JASONCHENG22.AU
   us-west-2.compute.internal = JASONCHENG22.AU
