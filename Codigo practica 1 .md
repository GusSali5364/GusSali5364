
        String sPinias = txtPinias.getText();
        int iPinias = Integer.parseInt(sPinias);
        String sMangos = txtMangos.getText();
        int iMangos = Integer.parseInt(sMangos);
        String sSandias = txtSandias.getText();
        int iSandias = Integer.parseInt(sSandias);
        String sCocos = txtCocos.getText();
        int iCocos = Integer.parseInt(sCocos);
        String sCerezas = txtCerezas.getText();
        int iCerezas = Integer.parseInt(sCerezas);
        
        double iPiniasSuma = (iPinias * 14.00);
        double iMangosSuma = (iMangos * 17.00);
        double iSandiasSuma = (iSandias * 8.00);
        double iCocosSuma = (iCocos * 9.00);
        double iCerezasSuma = (iCerezas * 21.00);
        
        double dSubTotal = (iPiniasSuma + iMangosSuma + iSandiasSuma + iCocosSuma + iCerezasSuma);
            txtSubTotal.setText(String.valueOf("$" + String.format("%.2f", dSubTotal))); 
        
        if (dSubTotal >= 500 && dSubTotal < 1000){ 
            String sDescuento = String.valueOf("$" + String.format("%.2f" , dSubTotal * 0.05));
            txtDescuento2.setText(sDescuento);
            txtDescuento.setText("5%");
            txtTotal.setText(String.valueOf("$" + String.format("%.2f", dSubTotal - (dSubTotal * 0.05)))); 
    }
        else if (dSubTotal >= 1000 && dSubTotal < 7000){ 
            String sDescuento = String.valueOf("$" + String.format("%.2f" , dSubTotal * 0.11));
            txtDescuento2.setText(sDescuento);
            txtDescuento.setText("11%");
            txtTotal.setText(String.valueOf("$" + String.format("%.2f", dSubTotal - (dSubTotal * 0.11))));          
    }
        else if (dSubTotal >= 7000 && dSubTotal < 15000){ 
            String sDescuento = String.valueOf("$" + String.format("%.2f" , dSubTotal * 0.18));
            txtDescuento2.setText(sDescuento);
            txtDescuento.setText("18%");
            txtTotal.setText(String.valueOf("$" + String.format("%.2f", dSubTotal - (dSubTotal * 0.18)))); 
    }
        else if (dSubTotal >= 15000){ 
            String sDescuento = String.valueOf("$" + String.format("%.2f" , dSubTotal * 0.25));
            txtDescuento2.setText(sDescuento);
            txtDescuento.setText("25%");
            txtTotal.setText(String.valueOf("$" + String.format("%.2f", dSubTotal - (dSubTotal * 0.25)))); 
    }
        else{  
            txtDescuento.setText(0 + "%");  
            txtDescuento2.setText("$0.00");
            txtTotal.setText(String.valueOf("$" +String.format("%.2f",dSubTotal)));
        }
    }                                          

    private void txtPiniasActionPerformed(java.awt.event.ActionEvent evt) {                                          
        // TODO add your handling code here:    
    }                                         

    private void txtSubTotalActionPerformed(java.awt.event.ActionEvent evt) {                                            
        // TODO add your handling code here:
    }                                           

    private void txtDescuentoActionPerformed(java.awt.event.ActionEvent evt) {                                             
        // TODO add your handling code here:
    }                                            

    private void txtDescuento2ActionPerformed(java.awt.event.ActionEvent evt) {                                              
        // TODO add your handling code here:
    }                                             

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
        txtCerezas.setText("0");
        txtCocos.setText("0");
        txtDescuento.setText("0");
        txtDescuento2.setText("0");
        txtMangos.setText("0");
        txtPinias.setText("0");
        txtSandias.setText("0");
        txtSubTotal.setText("0");
        txtTotal.setText("0");
    }                                 
