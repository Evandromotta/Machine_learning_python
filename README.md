public class Frota { 
    private String veiculo;
    private Carga liberadopParaCarregar;
    private Carga naoLiberadoParaCarregar;
    private int cargaCheia;
    private int quantidade;

    public Frota (String v, Carga lPC, Carga nLPC,int cC){
        veiculo = v;
        liberadopParaCarregar = lPC;
        naoLiberadoParaCarregar = nLPC;
        cargaCheia = cC;
    }
        
    public void setVeiculo(String v){
        veiculo = v;
    }
    public String getVeiculo(){
        return veiculo;
    }
        
    public void setCargaCheia(int cC){
        cargaCheia = cC;
    }
    public int getCargaCheia(){
        return cargaCheia;
    }
    
        public void setQuantidade(int q){
        quantidade = q;
    }
    public int getQuantidade(){
        return quantidade;
    }
 
    public boolean cargaCompleta(){
        if (cargaCheia == quantidade){
            return true;
        }
        return false;
    }
    
    public boolean carrega(){
        if (cargaCheia > quantidade){
            quantidade = quantidade + 1;
            return true;
        }
        return false;
    }
    
    public boolean descarrega(){
        quantidade = quantidade - 1;
        return true;
    }
    
    public void exibeInformacoesFrota(){
        System.out.println("Veículo: " + veiculo);
        System.out.println("Produto para carregar: " + liberadopParaCarregar.getProduto());
        System.out.println("Produto para descarregar: " + naoLiberadoParaCarregar.getProduto());
        System.out.println("Quantidade máxima de produtos por Frota: " + cargaCheia);
        System.out.println("Quantidade do carregamento atual: " + quantidade);
    }
}    
