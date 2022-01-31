# Practice427b
CodeForces Exercise
public class PrisonTransfer {
    
    public int getNroWaysToTransfer(List<Integer> conditions, List<Integer> prisoners) {
        int nroWays = 0;
        int nPrisoners = conditions.get(0);
        int tLimit = conditions.get(1);
        int cPrisoners = conditions.get(2);
        int i = 0;
        while(i + cPrisoners <= nPrisoners) {
            int aux = i + cPrisoners;
            if(levelIsAceptable(i, prisoners, aux, tLimit)) {
                nroWays ++;
            }else{}
            i ++ ;  
        }
        
        return nroWays;
    }
    
    private boolean levelIsAceptable(int ind, List<Integer> prisoners, int aux,int t){
        boolean isNotGreater = true;
        for(int i = ind; i < aux && isNotGreater; i++) {
            if(prisoners.get(i) > t) {
                isNotGreater = false;
            }else {}
        }
        return isNotGreater;
    }
}
