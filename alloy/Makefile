#--------------------------------------------------
# Makefile for Alloy CLI
#--------------------------------------------------

TYP := xml
OUT := out
ALLOY := alloy
SOLVER := minisat

%.run: %.als
	mkdir -p $(OUT) 
	rm -rf $(OUT)/$* && rm -rf $(OUT)/$< && cp $< $(OUT)/ 
	cd out && $(ALLOY) exec -t $(TYP) --solver $(SOLVER) $<

%.gui: %.als
	$(ALLOY) gui $<
