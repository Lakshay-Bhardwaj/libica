#OPTS = -O0 -g -Wall -fprofile-arcs -ftest-coverage -fPIC
#OPTS = -O0 -g -Wall -m31 -D_LINUX_S390_
OPTS = -O0 -g -Wall -D_LINUX_S390_
LIBS = -L../.libs
INCLUDE = -I. -I../include -I../../include
CC = gcc

TARGETS = icastats_test \
	  libica_des_test libica_3des_test \
	  libica_aes128_test libica_aes192_test libica_aes256_test \
	  libica_sha1_test \
	  libica_sha256_test \
	  libica_rsa_test libica_rng_test libica_keygen_test \
	  test_mech_list \
	  libica_cmac_test \
	  libica_aes_xts_test libica_aes_gcm_test libica_ccm_test \
	  libica_aes_ctr_test libica_aes_ofb_test libica_aes_cfb_test \
	  libica_aes_cbc_test libica_aes_ecb_test \
	  libica_des_ctr_test libica_3des_ctr_test \
	  libica_des_cfb_test libica_3des_cfb_test \
	  libica_des_cbc_test libica_3des_cbc_test \
	  libica_des_ecb_test libica_cbccs_test libica_3des_ecb_test \
	  libica_des_ofb_test libica_3des_ofb_test \
	  libica_get_version \
      libica_get_functionlist

all: $(TARGETS)

# Every target is created from a single .c file.
%: %.c
	gcc $(OPTS) $(LIBS) $(INCLUDE) -lica -lcrypto -o $@ $^

clean:
	rm -f $(TARGETS)

distclean:
	rm -f Makefile
	rm -f $(TARGETS)